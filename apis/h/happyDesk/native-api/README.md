# HappyDesk: Native API Reference

A consolidated summary of HappyDesk's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://staffy.happydesk.ru/api-docs/
- **OpenAPI specification:** https://staffy.happydesk.ru/api-docs/swagger.json
- **API base URL:** `{tenantUrl}/panel/api`

## Authentication

### API Token

Authenticate with a HappyDesk personal API token and your full HappyDesk workspace URL.

### Credentials

- **API Key:** `apiKey` · required
- **Tenant URL:** `tenantUrl` · required · Your full HappyDesk workspace URL, for example https://your-company.happydesk.ru

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://staffy.happydesk.ru/api-docs/)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Knowledge Categories](actions/get-all-knowledge-categories.md) | `GET /knowledge/all-categories` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get All Knowledge Instructions](actions/get-all-knowledge-instructions.md) | `GET /knowledge/all-instructions` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get All Knowledge Sections](actions/get-all-knowledge-sections.md) | `GET /knowledge/all-sections` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Company Settings](actions/get-company-settings.md) | `GET /v2/company-settings` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Current User](actions/get-current-user.md) | `GET /v2/user/me` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Issue Channels](actions/get-issue-channels.md) | `GET /issue/channel` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Issue Priorities](actions/get-issue-priorities.md) | `GET /issue/priority` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Issue Statuses](actions/get-issue-statuses.md) | `GET /issue/status` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Issue Templates](actions/get-issue-templates.md) | `GET /issue/template` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Issue Types](actions/get-issue-types.md) | `GET /issue/type` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Issues](actions/get-issues.md) | `GET /issue` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Knowledge Categories](actions/get-knowledge-categories.md) | `GET /knowledge/category` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Knowledge Instructions](actions/get-knowledge-instructions.md) | `GET /knowledge/instruction` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Knowledge Sections](actions/get-knowledge-sections.md) | `GET /knowledge/section` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Nested Issue Categories](actions/get-nested-issue-categories.md) | `GET /issue/category/nested` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Schedules](actions/get-schedules.md) | `GET /v2/schedule` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get System Environments](actions/get-system-environments.md) | `GET /v2/system/environments` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get User Company](actions/get-user-company.md) | `GET /user/company` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get User Groups](actions/get-user-groups.md) | `GET /v2/user/group` | [docs](https://staffy.happydesk.ru/api-docs/) |
| [Get Users](actions/get-users.md) | `GET /v2/users` | [docs](https://staffy.happydesk.ru/api-docs/) |
