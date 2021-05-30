---
layout: post
title: UTF-8 encoding issue in spring MVC Ajax
categories: SpringMVC
---

Recently I needed to work with a spring mvc project, with non-english characters (malayalam characters for eg.) The MySQL database table
was indeed utf-8 by default and we can directly enter the non-english characters in there easily. The problem being the response
from the controller was being shown as a string of characters like ???.

So begins with this [Stack Overflow answer](https://stackoverflow.com/questions/5649329/utf-8-encoding-problem-in-spring-mvc), there was a blog
page which offered three solutions. However the hosting was down, have to access it via [wayback machine](https://web.archive.org/web/20161110075036/http://charlie.cu.cc/2012/08/spring-mvc-ajax-request-with-utf-8-support/). I'm posting the first
solution here, because many replied that's the solution that worked for them.

**Solution 1**: Don’t use @ResponseBody. Return void in the controller, and use HtppServletResponse to return string with valid formatting.

here's my code
```
@RequestMapping("getRandomArticle")
public void getRandomArticle(
	HttpServletRequest request, HttpServletResponse response) throws IOException {

	response.addHeader("Content-Type", "text/html;charset=UTF-8");
	response.setCharacterEncoding("UTF-8");
	
	List stuffs = dao.getRandomData();
	
	ServletOutputStream responseClient = response.getOutputStream();
	
	String jsonString = new Gson().toJson(stuffs.get(0));
	byte[] utf8JsonString = jsonString.getBytes("UTF-8");
	responseClient.write(utf8JsonString);
	responseClient.close();
}
```

I hope this is helpful for someone out there :)
