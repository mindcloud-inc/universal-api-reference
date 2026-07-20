# Qlik: Native API Reference

A consolidated summary of Qlik's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://qlik.dev/apis/rest/
- **API base URL:** `https://{tenantHost}`

## Authentication

### OAuth2

Qlik Cloud OAuth2 machine-to-machine authentication for tenant REST APIs.

### Credentials

- **Tenant Host:** `tenantHost` · required · Your Qlik Cloud tenant host, without protocol. Example: example.us.qlikcloud.com

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.tenantHost}}/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.tenantHost}}/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user_default apps spaces.shared spaces.managed spaces.data users data-connections automations webhooks identity.name:read identity.email:read admin.apps admin.spaces admin.users admin.automations admin.webhooks`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://qlik.dev/authenticate/oauth/)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `links.next.href`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `next` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Item To Collection](actions/add-item-to-collection.md) | `POST /api/v1/collections/:collectionId/items` | [docs](https://qlik.dev/apis/rest/collections/) |
| [Assign Space Member](actions/assign-space-member.md) | `POST /api/v1/spaces/:spaceId/assignments` | [docs](https://qlik.dev/apis/rest/spaces/) |
| [Cancel Reload](actions/cancel-reload.md) | `POST /api/v1/reloads/:reloadId/actions/cancel` | [docs](https://qlik.dev/apis/rest/reloads/) |
| [Copy App](actions/copy-app.md) | `POST /api/v1/apps/:appId/copy` | [docs](https://qlik.dev/apis/rest/apps/) |
| [Count Users](actions/count-users.md) | `GET /api/v1/users/actions/count` | [docs](https://qlik.dev/apis/rest/users/) |
| [Create App](actions/create-app.md) | `POST /api/v1/apps` | [docs](https://qlik.dev/apis/rest/apps/) |
| [Create Collection](actions/create-collection.md) | `POST /api/v1/collections` | [docs](https://qlik.dev/apis/rest/collections/) |
| [Create Space](actions/create-space.md) | `POST /api/v1/spaces` | [docs](https://qlik.dev/apis/rest/spaces/) |
| [Export App](actions/export-app.md) | `POST /api/v1/apps/:appId/export` | [docs](https://qlik.dev/apis/rest/apps/) |
| [Filter Groups](actions/filter-groups.md) | `POST /api/v1/groups/actions/filter` | [docs](https://qlik.dev/apis/rest/groups/) |
| [Filter Users](actions/filter-users.md) | `POST /api/v1/users/actions/filter` | [docs](https://qlik.dev/apis/rest/users/) |
| [Get App](actions/get-app.md) | `GET /api/v1/apps/:appId` | [docs](https://qlik.dev/apis/rest/apps/) |
| [Get App Lineage](actions/get-app-lineage.md) | `GET /api/v1/apps/:appId/data/lineage` | [docs](https://qlik.dev/apis/rest/apps/) |
| [Get App Metadata](actions/get-app-metadata.md) | `GET /api/v1/apps/:appId/data/metadata` | [docs](https://qlik.dev/apis/rest/apps/) |
| [Get Collection](actions/get-collection.md) | `GET /api/v1/collections/:collectionId` | [docs](https://qlik.dev/apis/rest/collections/) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/users/me` | [docs](https://qlik.dev/apis/rest/users/#%23%2Fentries%2Fv1%2Fusers%2Fme-get) |
| [Get Favorites Collection](actions/get-favorites-collection.md) | `GET /api/v1/collections/favorites` | [docs](https://qlik.dev/apis/rest/collections/) |
| [Get Group](actions/get-group.md) | `GET /api/v1/groups/:groupId` | [docs](https://qlik.dev/apis/rest/groups/) |
| [Get Item](actions/get-item.md) | `GET /api/v1/items/:itemId` | [docs](https://qlik.dev/apis/rest/items/) |
| [Get Reload](actions/get-reload.md) | `GET /api/v1/reloads/:reloadId` | [docs](https://qlik.dev/apis/rest/reloads/) |
| [Get Space](actions/get-space.md) | `GET /api/v1/spaces/:spaceId` | [docs](https://qlik.dev/apis/rest/spaces/) |
| [Get User](actions/get-user.md) | `GET /api/v1/users/:userId` | [docs](https://qlik.dev/apis/rest/users/) |
| [List Collection Items](actions/list-collection-items.md) | `GET /api/v1/collections/:collectionId/items` | [docs](https://qlik.dev/apis/rest/collections/) |
| [List Collections](actions/list-collections.md) | `GET /api/v1/collections` | [docs](https://qlik.dev/apis/rest/collections/) |
| [List Groups](actions/list-groups.md) | `GET /api/v1/groups` | [docs](https://qlik.dev/apis/rest/groups/) |
| [List Item Collections](actions/list-item-collections.md) | `GET /api/v1/items/:itemId/collections` | [docs](https://qlik.dev/apis/rest/items/) |
| [List Items](actions/list-items.md) | `GET /api/v1/items` | [docs](https://qlik.dev/apis/rest/items/) |
| [List Published Items](actions/list-published-items.md) | `GET /api/v1/items/:itemId/publisheditems` | [docs](https://qlik.dev/apis/rest/items/) |
| [List Reload Tasks](actions/list-reload-tasks.md) | `GET /api/v1/reload-tasks` | [docs](https://qlik.dev/apis/rest/reload-tasks/) |
| [List Reloads](actions/list-reloads.md) | `GET /api/v1/reloads` | [docs](https://qlik.dev/apis/rest/reloads/) |
| [List Space Assignments](actions/list-space-assignments.md) | `GET /api/v1/spaces/:spaceId/assignments` | [docs](https://qlik.dev/apis/rest/spaces/) |
| [List Space Types](actions/list-space-types.md) | `GET /api/v1/spaces/types` | [docs](https://qlik.dev/apis/rest/spaces/) |
| [List Spaces](actions/list-spaces.md) | `GET /api/v1/spaces` | [docs](https://qlik.dev/apis/rest/spaces/) |
| [List Users](actions/list-users.md) | `GET /api/v1/users` | [docs](https://qlik.dev/apis/rest/users/) |
| [Trigger App Reload](actions/trigger-app-reload.md) | `POST /api/v1/reloads` | [docs](https://qlik.dev/apis/rest/reloads/) |
| [Update App](actions/update-app.md) | `PUT /api/v1/apps/:appId` | [docs](https://qlik.dev/apis/rest/apps/) |
| [Update Collection](actions/update-collection.md) | `PUT /api/v1/collections/:collectionId` | [docs](https://qlik.dev/apis/rest/collections/) |
| [Update Item](actions/update-item.md) | `PUT /api/v1/items/:itemId` | [docs](https://qlik.dev/apis/rest/items/) |
| [Update Space Assignment](actions/update-space-assignment.md) | `PUT /api/v1/spaces/:spaceId/assignments/:assignmentId` | [docs](https://qlik.dev/apis/rest/spaces/) |
| [Update Space Properties](actions/update-space-properties.md) | `PATCH /api/v1/spaces/:spaceId` | [docs](https://qlik.dev/apis/rest/spaces/) |
