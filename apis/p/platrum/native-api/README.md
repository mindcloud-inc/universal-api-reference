# Platrum: Native API Reference

A consolidated summary of Platrum's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** http://api.docs.platrum.ru
- **API base URL:** `https://3e8e7be.platrum.com`

## Authentication

### API Key

Use a Platrum project API key. Platrum requires the key to be sent in the Api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](http://api.docs.platrum.ru/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive space](actions/archive-space.md) | `POST /wiki/api/space/archive` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
| [Create task](actions/create-task.md) | `POST /tasks/api/task/create` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [Delete article](actions/delete-article.md) | `POST /wiki/api/article/delete` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
| [Delete board](actions/delete-board.md) | `POST /tasks/api/board/delete` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [Get article](actions/get-article.md) | `POST /wiki/api/article/get` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
| [Get exchange rate](actions/get-exchange-rate.md) | `POST /finance/api/currency/exchange-rate` | [docs](http://api.docs.platrum.ru/modules/finance/) |
| [Get task](actions/get-task.md) | `POST /tasks/api/task/get` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [List active currencies](actions/list-active-currencies.md) | `POST /finance/api/currency/list-active` | [docs](http://api.docs.platrum.ru/modules/finance/) |
| [List active workers](actions/list-active-workers.md) | `POST /orgschema/api/worker/list-active` | [docs](http://api.docs.platrum.ru/modules/orgschema/) |
| [List articles](actions/list-articles.md) | `POST /wiki/api/article/list` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
| [List board tasks](actions/list-board-tasks.md) | `POST /tasks/api/board/task/list` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [List budget requests](actions/list-budget-requests.md) | `POST /finplan/api/request/list` | [docs](http://api.docs.platrum.ru/modules/finplan/) |
| [List cashboxes](actions/list-cashboxes.md) | `POST /finance/api/transaction/cashbox-list` | [docs](http://api.docs.platrum.ru/modules/finance/) |
| [List courses](actions/list-courses.md) | `POST /wiki/api/course/list` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
| [List currencies](actions/list-currencies.md) | `POST /finance/api/currency/list` | [docs](http://api.docs.platrum.ru/modules/finance/) |
| [List finance categories](actions/list-finance-categories.md) | `POST /fintransaction/api/category/list` | [docs](http://api.docs.platrum.ru/modules/finance/) |
| [List item categories](actions/list-item-categories.md) | `POST /store/api/item/category/list` | [docs](http://api.docs.platrum.ru/modules/store/) |
| [List org blocks](actions/list-org-blocks.md) | `POST /orgschema/api/block/list` | [docs](http://api.docs.platrum.ru/modules/orgschema/) |
| [List password categories](actions/list-password-categories.md) | `POST /password/api/category/list` | [docs](http://api.docs.platrum.ru/modules/password/) |
| [List passwords](actions/list-passwords.md) | `POST /password/api/password/list` | [docs](http://api.docs.platrum.ru/modules/password/) |
| [List profiles](actions/list-profiles.md) | `POST /user/api/profile/list` | [docs](http://api.docs.platrum.ru/modules/user/#_2) |
| [List schedules](actions/list-schedules.md) | `POST /user/api/schedule/list` | [docs](http://api.docs.platrum.ru/modules/user/) |
| [List spaces](actions/list-spaces.md) | `POST /wiki/api/space/list` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
| [List staff](actions/list-staff.md) | `POST /company/api/staff/list` | [docs](http://api.docs.platrum.ru/modules/company/) |
| [List store items](actions/list-store-items.md) | `POST /store/api/item/list` | [docs](http://api.docs.platrum.ru/modules/store/) |
| [List task boards](actions/list-task-boards.md) | `POST /tasks/api/board/list` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [List tasks](actions/list-tasks.md) | `POST /tasks/api/task/list` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [List workers](actions/list-workers.md) | `POST /orgschema/api/worker/list` | [docs](http://api.docs.platrum.ru/modules/orgschema/) |
| [Remove task](actions/remove-task.md) | `POST /tasks/api/task/remove` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [Save article](actions/save-article.md) | `POST /wiki/api/article/save` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
| [Save board](actions/save-board.md) | `POST /tasks/api/board/store` | [docs](http://api.docs.platrum.ru/modules/tasks/) |
| [Save counterparty](actions/save-counterparty.md) | `POST /fintransaction/api/counterparty/save` | [docs](http://api.docs.platrum.ru/modules/finance/) |
| [Save space](actions/save-space.md) | `POST /wiki/api/space/save` | [docs](http://api.docs.platrum.ru/modules/wiki/) |
