# Priority Matrix: Native API Reference

A consolidated summary of Priority Matrix's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://sync.appfluence.com/developer/guide/
- **API base URL:** `https://sync.appfluence.com`

## Authentication

### OAuth2

Connect with a registered Priority Matrix OAuth application.

### Credentials

- **Priority Matrix Username:** `username` · required · The email address used to sign in to Priority Matrix.
- **Priority Matrix Password:** `password` · required · The password used to sign in to Priority Matrix.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://sync.appfluence.com/o/token/.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write collaborators`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://sync.appfluence.com/developer/guide/)

## API conventions

The next-page cursor is read from `meta.next`.

## Pagination

Use `limit` in the query string to set the page size (default 30). Use `offset` in the query string as the record offset; numbering starts at 0. Follow the complete next-page URL returned by the API.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Item Comment](actions/add-item-comment.md) | `POST /api/v1/comment/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Add Item Tag](actions/add-item-tag.md) | `POST /api/v1/tag/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Add Project Tag](actions/add-project-tag.md) | `POST /api/v1/tag/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Create Inbox Item](actions/create-inbox-item.md) | `POST /api/v1/item/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Create Project](actions/create-project.md) | `POST /api/v1/project/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [Create Project Item](actions/create-project-item.md) | `POST /api/v1/item/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Create Project Webhook](actions/create-project-webhook.md) | `POST /api/v1/hook/` | [docs](https://sync.appfluence.com/developer/guide/#webhooks) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v1/hook/` | [docs](https://sync.appfluence.com/developer/guide/#webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v1/hook/:id/` | [docs](https://sync.appfluence.com/developer/guide/#webhooks) |
| [Find Items By Date](actions/find-items-by-date.md) | `GET /api/v1/item/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Find Items By Tag](actions/find-items-by-tag.md) | `GET /api/v1/item/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [Find Projects By Creation Date](actions/find-projects-by-creation-date.md) | `GET /api/v1/project/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Find Projects By Schedule Date](actions/find-projects-by-schedule-date.md) | `GET /api/v1/project/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Find Projects By Tag](actions/find-projects-by-tag.md) | `GET /api/v1/project/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [Get Account](actions/get-account.md) | `GET /api/v1/account/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/account) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/me/` | [docs](https://sync.appfluence.com/developer/guide/) |
| [Get Item](actions/get-item.md) | `GET /api/v1/item/:id/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/item) |
| [Get Project](actions/get-project.md) | `GET /api/v1/project/:idd/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/project) |
| [Get User](actions/get-user.md) | `GET /api/v1/user/:id/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/user) |
| [List Account Members](actions/list-account-members.md) | `GET /api/v1/account/users/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Active Projects](actions/list-active-projects.md) | `GET /api/v1/project/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/project) |
| [List Collaborators](actions/list-collaborators.md) | `GET /api/v1/me/collaborators/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Completed Project Items](actions/list-completed-project-items.md) | `GET /api/v1/project/:idd/items/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Inbox Items](actions/list-inbox-items.md) | `GET /api/v1/me/inbox/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Item Comments](actions/list-item-comments.md) | `GET /api/v1/item/:id/comments` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [List Item Followers](actions/list-item-followers.md) | `GET /api/v1/item/:id/followers` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Item Tags](actions/list-item-tags.md) | `GET /api/v1/item/:id/tags` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Items](actions/list-items.md) | `GET /api/v1/item/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/item) |
| [List Project Item Summaries](actions/list-project-item-summaries.md) | `GET /api/v1/project/:idd/item_summaries/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Project Items](actions/list-project-items.md) | `GET /api/v1/project/:idd/items/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Project Items By Quadrant](actions/list-project-items-by-quadrant.md) | `GET /api/v1/project/:idd/items/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Project Owners](actions/list-project-owners.md) | `GET /api/v1/project/:idd/owners/` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Project Tags](actions/list-project-tags.md) | `GET /api/v1/project/:idd/tags` | [docs](https://sync.appfluence.com/developer/guide/#common-api) |
| [List Users](actions/list-users.md) | `GET /api/v1/user/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/user) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v1/hook/` | [docs](https://sync.appfluence.com/developer/guide/#webhooks) |
| [Remove Item Tag](actions/remove-item-tag.md) | `POST /api/v1/tag/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Remove Project Tag](actions/remove-project-tag.md) | `POST /api/v1/tag/` | [docs](https://sync.appfluence.com/developer/guide/#concrete-examples) |
| [Update Item](actions/update-item.md) | `PUT /api/v1/item/:id/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/item) |
| [Update Item Notes](actions/update-item-notes.md) | `PUT /api/v1/item/:id/` | [docs](https://sync.appfluence.com/api/v1/docs/#!/item) |
| [Update Webhook](actions/update-webhook.md) | `PUT /api/v1/hook/:id/` | [docs](https://sync.appfluence.com/developer/guide/#webhooks) |
