# <img src="https://images.mindcloud.co/apps/icons/geotab_1785526269980.png" alt="Geotab logo" width="28" height="28"> Geotab: Universal API

Manage fleets, assets, users, groups, zones, and operational data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/geotab/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.geotab.com
- **Vendor API docs:** https://developers.geotab.com/myGeotab/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate](actions/authenticate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geotab/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Asset Group

| Action | Method | Description |
| --- | --- | --- |
| [List Asset Groups](actions/list-asset-groups.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET |  |
| [Count Asset Groups](actions/count-asset-groups.md) | GET |  |
| [Count Assets](actions/count-assets.md) | GET |  |
| [Create Asset](actions/create-asset.md) | POST |  |
| [Create Asset Group](actions/create-asset-group.md) | POST |  |
| [Delete Asset](actions/delete-asset.md) | DELETE |  |
| [Delete Asset Group](actions/delete-asset-group.md) | DELETE |  |
| [Get Asset](actions/get-asset.md) | GET |  |
| [Get Asset Feed](actions/get-asset-feed.md) | GET |  |
| [Get Asset Group](actions/get-asset-group.md) | GET |  |
| [List Assets](actions/list-assets.md) | GET |  |
| [Update Asset](actions/update-asset.md) | PUT |  |
| [Update Asset Group](actions/update-asset-group.md) | PUT |  |

