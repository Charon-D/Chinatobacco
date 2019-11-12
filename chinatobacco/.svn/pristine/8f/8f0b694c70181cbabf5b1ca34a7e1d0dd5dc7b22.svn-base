<%@ page language="java" contentType="text/html; charset=UTF-8"
	pageEncoding="UTF-8"%>
<%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c"%>
<%@ taglib uri="http://java.sun.com/jsp/jstl/fmt" prefix="fmt"%>

<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>商户个人信息展示</title>
<c:import url="common.jsp"></c:import>
</head>
<body>

	<c:import url="navuser.jsp"></c:import>
	<div style="margin: 0 5%">
		<form action="" method="post">
			<h1>订单信息展示</h1>
			<table class="table table-hover">
				<tr>
					<th><input type="checkbox" /></th>
					<th>订单编号</th>
					<th>商品名称</th>
					<th>总价</th>
					<th>创建时间</th>
					<th>成交时间</th>
					<th>状态</th>
					<th>支付单号</th>
				</tr>
				<c:forEach var="list" items="${list}">
					<tr>
						<td><input name="storeid" type="checkbox"
							value="${list.indentid }" /></td>
						<td>${list.cbaglist.commodity.comname }</td>
						<td>${list.grossprice }</td>
						<td>${list.createdate}</td>
						<td>${list.enddate}</td>
						<td>${list.indentstate.statename}</td>
						<td>${list.payid}</td>
						
						<td><input
							onclick="javascript:location.href='update.do?id=${list.storeid}'"
							value="修改" type="button" /></td>
					</tr>
				</c:forEach>

			</table>
			<div class="form-group d1">
				<div class="col-sm-offset-2 col-sm-10">
					<a href=""><input class="btn btn-default"
						style="margin-left: 30%;" type="button" value="添加" /></a>
					<button type="submit" class="btn btn-default">删除</button>
				</div>
			</div>

		</form>
	</div>
	<c:import url="foot.jsp"></c:import>
</body>
</html>
