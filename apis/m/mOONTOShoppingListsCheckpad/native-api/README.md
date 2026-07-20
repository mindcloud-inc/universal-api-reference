# MOONTO Shopping Lists - Checkpad: Native API Reference

A consolidated summary of MOONTO Shopping Lists - Checkpad's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://api.moonto.app/docs
- **OpenAPI specification:** https://api.moonto.app/openapi.json
- **API base URL:** `https://api.moonto.app`

## Authentication

### MOONTO OAuth2

OAuth2 authorization code bearer token for the official MOONTO API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.moonto.app/auth/authorization to approve access.
2. Exchange the returned authorization code with a POST request to https://api.moonto.app/auth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://api.moonto.app/docs)

## Pagination

Use `limit` in the query string to set the page size (default 50; minimum 1). Use `cursor` in the query string as the pagination cursor.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add List Item](actions/add-list-item.md) | `PUT /lists/{list_id}/add` | [docs](https://api.moonto.app/docs#/Lists/add_list_item_lists__list_id__add_put) |
| [Check List Item](actions/check-list-item.md) | `PUT /lists/{list_id}/check` | [docs](https://api.moonto.app/docs#/Lists/check_list_item_lists__list_id__check_put) |
| [Delete List Item](actions/delete-list-item.md) | `DELETE /lists/{list_id}/delete` | [docs](https://api.moonto.app/docs#/Lists/delete_list_item_lists__list_id__delete_delete) |
| [Get Checkpad Details](actions/get-checkpad-details.md) | `GET /checkpads/{checkpad_id}` | [docs](https://api.moonto.app/docs#/Checkpads/get_checkpad_details_checkpads__checkpad_id__get) |
| [Get List Details](actions/get-list-details.md) | `GET /lists/{list_id}` | [docs](https://api.moonto.app/docs#/Lists/get_list_details_lists__list_id__get) |
| [List Checkpad Events](actions/list-checkpad-events.md) | `GET /checkpads/{checkpad_id}/events` | [docs](https://api.moonto.app/docs#/Checkpads/get_checkpad_events_checkpads__checkpad_id__events_get) |
| [List Checkpads](actions/list-checkpads.md) | `GET /checkpads/` | [docs](https://api.moonto.app/docs#/Checkpads/get_checkpads_checkpads__get) |
| [List List Events](actions/list-list-events.md) | `GET /lists/{list_id}/events` | [docs](https://api.moonto.app/docs#/Lists/get_list_events_lists__list_id__events_get) |
| [List List Items](actions/list-list-items.md) | `GET /lists/{list_id}/items` | [docs](https://api.moonto.app/docs#/Lists/get_list_items_lists__list_id__items_get) |
| [List Lists](actions/list-lists.md) | `GET /lists/` | [docs](https://api.moonto.app/docs#/Lists/get_lists_lists__get) |
