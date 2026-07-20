# GoDial: Native API Reference

A consolidated summary of GoDial's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://godial.stoplight.io/docs/godial/cd4edf0828dd6-go-dial-crm-external-api
- **API base URL:** `https://enterprise.godial.cc/meta/api`

## Authentication

### API key

Use the GoDial External API access token from Dashboard > Integration > External API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://godial.cc/blog/integrating-your-website-or-crm-with-godial-using-api/)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create User](actions/accounts-add.md) | `POST /externals/accounts/add` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1Ng-accounts-add) |
| [List Users](actions/accounts-list.md) | `GET /externals/accounts/list` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1NA-accounts-list) |
| [Delete User](actions/accounts-remove.md) | `DELETE /externals/accounts/[:id]/remove` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1Nw-accounts-remove) |
| [Update User](actions/accounts-update.md) | `PUT /externals/accounts/[:id]/update` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1OA-accounts-update) |
| [Get User](actions/accounts-view.md) | `GET /externals/accounts/[:id]/view` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1NQ-accounts-view) |
| [Create Contact](actions/contact-add.md) | `POST /externals/contact/add` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2Mg-contact-add) |
| [Move Contact to List](actions/contact-change-list.md) | `POST /externals/contact/listchange` | [docs](https://godial.stoplight.io/docs/godial/b3A6NTg1NTgyNDE3-contact-change-list) |
| [Delete Contact by Phone Number](actions/contact-delete-by-phone-number.md) | `POST /externals/contact/delete-by-phone` | [docs](https://godial.stoplight.io/docs/godial/b3A6NzkzMDk0NTM4-contact-delete-by-phone-number) |
| [Log Contact Disposition](actions/contact-dispose.md) | `POST /externals/contact/[:id]/dispose` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2NQ-contact-dispose) |
| [List Contacts](actions/contact-list.md) | `GET /externals/contact/list/[:listId]` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2MA-contact-list) |
| [Delete Contact](actions/contact-remove.md) | `DELETE /externals/contact/[:id]/remove` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2Mw-contact-remove) |
| [Update Contact](actions/contact-update.md) | `PUT /externals/contact/[:id]/update` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2NA-contact-update) |
| [Get Contact](actions/contact-view.md) | `GET /externals/contact/[:id]/view` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2MQ-contact-view) |
| [Create Contact List](actions/lists-add.md) | `POST /externals/lists/add` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2OA-lists-add) |
| [Assign Contact List to User](actions/lists-assign.md) | `POST /externals/lists/assign` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY3MQ-lists-assign) |
| [Unassign Contact List from User](actions/lists-detach.md) | `DELETE /externals/lists/detach` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY3Mg-lists-detach) |
| [List Contact Lists](actions/lists-list.md) | `GET /externals/lists/list` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2Ng-lists-list) |
| [Delete Contact List](actions/lists-remove.md) | `DELETE /externals/lists/[:id]/remove` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY3MA-lists-remove) |
| [Update Contact List](actions/lists-update.md) | `PUT /externals/lists/[:id]/update` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2OQ-lists-update) |
| [Get Contact List](actions/lists-view.md) | `GET /externals/lists/[:id]/view` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2Nw-lists-view) |
| [List Call Logs](actions/log-list.md) | `POST /externals/log/list` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY3Mw-log-list) |
| [Create Task](actions/task-add.md) | `POST /externals/tasks/add` | [docs](https://godial.stoplight.io/docs/godial/b3A6NzQwMTQ0NQ-task-add) |
| [List Tasks](actions/task-list.md) | `GET /externals/tasks/list` | [docs](https://godial.stoplight.io/docs/godial/b3A6NzQwMTQ0Mw-task-list) |
| [Delete Task](actions/task-remove.md) | `DELETE /externals/tasks/[:id]/remove` | [docs](https://godial.stoplight.io/docs/godial/b3A6NzQwMTQ0Nw-task-remove) |
| [Update Task](actions/task-update.md) | `PUT /externals/tasks/[:id]/update` | [docs](https://godial.stoplight.io/docs/godial/b3A6NzQwMTQ0Ng-task-update) |
| [Get Task](actions/task-view.md) | `GET /externals/tasks/[:id]/view` | [docs](https://godial.stoplight.io/docs/godial/b3A6NzQwMTQ0NA-task-view) |
| [Create Team](actions/team-add.md) | `POST /externals/team/add` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1MQ-team-add) |
| [List Teams](actions/team-list.md) | `GET /externals/team/list` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY0OQ-team-list) |
| [Delete Team](actions/team-remove.md) | `DELETE /externals/team/[:id]/remove` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1Mg-team-remove) |
| [Update Team](actions/team-update.md) | `PUT /externals/team/[:id]/update` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1Mw-team-update) |
| [Get Team](actions/team-view.md) | `GET /externals/team/[:id]/view` | [docs](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY1MA-team-view) |
