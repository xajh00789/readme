# DaoCloud Service License Admin
---

## API
### application API
application API为Jira用户登录DCS License Application后访问的API:

- 查看、post提交申请license页面 `/api/applications/`
- 查看申请license的详情页面 `/api/applications/<application_id>`


**参数说明**

| 参数名 | 类型 | 说明 |
| --- | --- | --- |
| JIRA_HOST | String | 安装有Jira的主机IP加端口 |
| JIRA_CONSUMER_KEY | String | Jira主机上配置的dcs提供的consumer秘钥 |
| JIRA_PRIVATE_RSA_KEY | String | 与Jira主机相匹配的非对称秘钥的私钥 |
| LICENSE_SERVER_URL | String | 对内API的服务器URL |
| X_DAO_INTERNAL_TOKEN | String | 对内 API，所有 API 都需要 X-DAO-INTERNAL-TOKEN |
| FERNET_KEY | String | 邮件发送中token生成种子 |
| ADMIN_USERNAME | String | Django自带admin的默认账户 |
| ADMIN_PASSWORD | String | Django自带admin的默认密码 |

### supervisor API
supervisor API为admin用户登录DCS License后访问的API：

- dcs license邮件批准、拒绝审核API `/approval/`