# <img src="https://images.mindcloud.co/apps/icons/storerocket_1776270407841.png" alt="Storerocket logo" width="28" height="28"> Storerocket: Universal API

StoreRocket is a hosted store locator platform. This app wraps the verified StoreRocket REST API for account info, project listing, and location CRUD.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/storerocket/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://storerocket.io
- **Vendor API docs:** https://storerocket.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [Delete Location](actions/delete-location.md) | DELETE |  |
| [Get Location](actions/get-location.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |
| [Update Location](actions/update-location.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET |  |

