# please remember to perform npm install command and execute node api.js on cmd

## 接口说明

- 接口地址：http://localhost:3000
- 接口已开启 CORS
- 接口认证统一使用 Token 认证（基于 JSON Web Token）
- 需要授权的接口必须提供请求头字段 X-Access-Token 信息
- 使用 HTTP Status Code 标识状态
- 分页列表参数使用 _page 和 _limit
- 时间日期格式：2017-12-24 13:52:26
- 数据返回格式统一使用 JSON
- 无特殊说明，接口默认支持 application/x-www-form-urlencoded 和 application/json 两种方式

### 通用的返回状态码说明

| 状态码 |                 含义                 |                 说明                 |
|--------|--------------------------------------|--------------------------------------|
|    200 | OK                                   | 请求成功                             |
|    201 | CREATED                              | 创建成功                             |
|    204 | DELETED                              | 删除成功                             |
|    400 | BAD REQUEST                          | 请求的地址不存在或者包含不支持的参数 |
|    401 | UNAUTHORIZED                         | 未授权                               |
|    403 | FORBIDDEN                            | 被禁止访问                           |
|    404 | NOT FOUND                            | 请求的资源不存在                     |
|    422 | Unprocesable entity [POST/PUT/PATCH] | 当创建一个对象时，发生一个验证错误   |
|    500 | INTERNAL SERVER ERROR                | 服务器内部错误                       |

### 返回结果说明

- GET /collection：返回资源对象的列表（数组）
- GET /collection/resource：返回单个资源对象
- POST /collection：返回新生成的资源对象
- PUT /collection/resource：返回完整的资源对象
- PATCH /collection/resource：返回完整的资源对象
- DELETE /collection/resource：返回一个空文档

### 通用错误返回结果

发生错误时，HTTP Status Code为4xx错，如 400，403，404

错误格式：

```json
{
  error: 'username invalid'
}
```

## 用户模块

### 用户注册

- POST
- `/users`

|   参数   | 是否必须 |     说明     |
|----------|----------|--------------|
| email    | 是       | 邮箱，用户名 |
| password | 是       | 密码         |

### 用户登陆

- 请求方法：POST
- 请求路径：`/session`

|   参数   | 是否必须 |     说明     |
|----------|----------|--------------|
| email    | 是       | 邮箱，用户名 |
| password | 是       | 密码         |

### 用户退出

- 请求方法：DELETE
- 请求路径：`/session`

## 联系人分类

### 获取分类列表

- 请求方法：`GET`
- 请求路径：`/tags`

### 新增分类

- 请求方法：`POST`
- 请求路径：`/tags`

### 编辑分类

- 请求方法：`POST`
- 请求路径：`/tags/:id`

### 删除分类

- 请求方法：`DELETE`
- 请求路径：`/tags/:id`

---

## 联系人

### 联系人列表

- 请求方法：`GET`
- 请求路径：`/contacts`

### 新增联系人

- 请求方法：`POST`
- 请求路径：`/contacts`

### 编辑联系人

- 请求方法：`PATCH`
- 请求路径：`/contacts/:id`

### 删除联系人

- 请求方法：`DELETE`
- 请求路径：`/contacts/:id`

#The address book case interface documentation

##Interface Description

- Interface address: http://localhost:3000
- Interface turned on CORS
- Interface authentication unified use of Token authentication (based on JSON Web Token)
- Interfaces that need authorization must provide request header field X-Access-Token information
- Identity status with HTTP Status Code
- Paging list parameters using _page and _limit
- Time Date Format: 2017-12-24 13:52:26
- Data return format unified use JSON
- No special instructions, interface default support application/x-www-form-urlencoded and application/json two ways

General return status code description

| Status Code . . .                 What it means                 Description . . .
|--------|--------------------------------------|--------------------------------------|
|    200 . . . OK . . . The request was successful.
|    201 . . . CREATED . . . Successful creation . . .
|    204 . . . DELETEDED . . . Successful deletion
|    400 . . . BAD REQUEST . . . The requested address does not exist or contains unsupported parameters . . .
|    401 . . . D'DD. Unauthorized . . .
|    403 . . . FORBIDDEN . . . Prohibited Access . . .
|    404 . . . NOT FOUND . . . The requested resource does not exist.
|    422 . . . Unprocesable entity (POST/PUT/PATCH) When an object is created, a validation error occurs.
|    500 . . . INTERNAL SERVER ERROR Internal errors on the server . . .

Return results description

- GET /collection: returns a list of resource objects (array)
- GET /collection/resource: Returns a single resource object
- POST /collection: returns newly generated resource objects
- PUT/collection/resource: Returns full resource object
- PATCH /collection/resource: Returns full resource object
- DELETE /collection/resource: Returns an empty document

Universal error return results

HTTP Status Code is 4xx error when an error occurs, such as 400,403,404

Wrong format:

'Json'
{
  error: 'username invalid'
}
```

User module

User registration

- POST
- '/users'

|   Parameters . . . Whether it is necessary to     Description . . .
|----------|----------|--------------|
| email . . . Yes, it's a Email, username . . .
| password . . . Yes, it's a Passwords . . .

User login

- Request method: POST
- Request path: '/session'

|   Parameters . . . Whether it is necessary to     Description . . .
|----------|----------|--------------|
| email . . . Yes, it's a Email, username . . .
| password . . . Yes, it's a Passwords . . .

User exit

- Request method: DELETE
- Request path: '/session'

Contact Category

Get a list of categories

- Request method: 'GET'
- Request path: '/tags'

New category

- Request method: 'POST'
- Request path: '/tags'

Edit edit edited category

- Request method: 'POST'
- Request path: '/tags/:id'

Delete the category

- Request method: 'DELETE'
- Request path: '/tags/:id'

---

Contacts

Contact list

- Request method: 'GET'
- Request path: '/contacts'

New Contacts

- Request method: 'POST'
- Request path: '/contacts'

Edit contact

- Request method: 'PATCH'
- Request path: '/contacts/:id'

Delete contacts

- Request method: 'DELETE'
- Request path: '/contacts/:id'