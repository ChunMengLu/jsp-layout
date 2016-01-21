## 说明
源码来自`rapid-framework`中的`rapid_jsp_extends`

为了自己和小伙伴使用方便而提交到git和maven！

## 使用说明
###maven
```xml
<dependency>
	<groupId>net.dreamlu</groupId>
	<artifactId>jsp-layout</artifactId>
	<version>0.0.2</version>
</dependency>
```

###_layout.jsp
```html
<%@ page language="java" session="false" contentType="text/html;charset=UTF-8" isELIgnored="false"%>
<%@ page trimDirectiveWhitespaces="true" %>
<%@ taglib prefix="layout" uri="http://www.dreamlu.net/tags/jsp-layout.tld" %>
<%-- 布局 --%>
<!DOCTYPE html>
<html>
<head>
	<%--重写的head --%>
	<layout:block name="head"></layout:block>
</head>
<body>
	<%--主体部分 --%>
	<layout:block name="content"></layout:block>
	<%--脚本部分--%>
	<layout:block name="script"></layout:block>
</body>
</html>
```
###index.jsp
```html
<%@ page language="java" session="false" contentType="text/html;charset=UTF-8" isELIgnored="false"%>
<%@ page trimDirectiveWhitespaces="true" %>
<%@ taglib prefix="layout" uri="http://www.dreamlu.net/tags/jsp-layout.tld" %>
<%-- 填充head --%>
<layout:override name="head">
    <title>head</title>
</layout:override>
<%-- 填充content --%>
<layout:override name="content">
    content
</layout:override>
<%-- 填充script --%>
<layout:override name="script">
    script
</layout:override>
<%@ include file="_layout.jsp" %>
```

## 交流群
如梦技术：[`237587118`](http://shang.qq.com/wpa/qunwpa?idkey=f78fcb750b4f72c92ff4d375d2884dd69b552301a1f2681af956bd32700eb2c0)

## 捐助共勉
<img src="http://soft.dreamlu.net/weixin-9.jpg" width = "200" alt="微信捐助" align=center />
<img src="http://soft.dreamlu.net/weixin-19.jpg" width = "200" alt="微信捐助" align=center />
<img src="http://soft.dreamlu.net/alipay.png" width = "200" alt="支付宝捐助" align=center />

<img src="http://soft.dreamlu.net/qq-9.jpg" width = "200" alt="QQ捐助" align=center />
<img src="http://soft.dreamlu.net/qq-19.jpg" width = "200" alt="QQ捐助" align=center />

## License

( The MIT License )