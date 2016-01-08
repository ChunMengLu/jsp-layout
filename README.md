## 说明
源码来自`rapid-framework`中的`rapid_jsp_extends`

为了自己和小伙伴使用方便而提交到git和maven！

## 使用说明
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

## License

( The MIT License )