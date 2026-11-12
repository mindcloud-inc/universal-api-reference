# Geotab: Native API Reference

A consolidated summary of Geotab's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://developers.geotab.com/myGeotab/introduction/
- **API base URL:** `https://{server}/apiv1`

## Authentication

### MyGeotab

Connect with a MyGeotab database user.

### Credentials

- **Server:** `server` · required · The MyGeotab server hostname. Use my.geotab.com unless authentication returns a different server path.
- **Database:** `database` · required · The MyGeotab database name.
- **Username:** `userName` · required · The username, typically an email address, for the MyGeotab API user.
- **Password:** `password` · required · The password for the MyGeotab API user.

[Official authentication documentation](https://developers.geotab.com/myGeotab/guides/concepts/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Authenticate/) |
| [Count Asset Groups](actions/count-asset-groups.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/GetCountOf/) |
| [Count Assets](actions/count-assets.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/GetCountOf/) |
| [Create Asset](actions/create-asset.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Add/) |
| [Create Asset Group](actions/create-asset-group.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Add/) |
| [Delete Asset](actions/delete-asset.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Remove/) |
| [Delete Asset Group](actions/delete-asset-group.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Remove/) |
| [Get Asset](actions/get-asset.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Get/) |
| [Get Asset Feed](actions/get-asset-feed.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/GetFeed/) |
| [Get Asset Group](actions/get-asset-group.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Get/) |
| [List Asset Groups](actions/list-asset-groups.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Get/) |
| [List Assets](actions/list-assets.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Get/) |
| [Update Asset](actions/update-asset.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Set/) |
| [Update Asset Group](actions/update-asset-group.md) | `POST` | [docs](https://developers.geotab.com/myGeotab/apiReference/methods/Set/) |
