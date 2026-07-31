# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423667345.png" alt="Open Notify logo" width="28" height="28"> Open Notify: Universal API

Open Notify through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openNotify/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current ISS Position](actions/get-current-iss-position.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-current-iss-position?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Iss Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Current ISS Position](actions/get-current-iss-position.md) | GET |  |

### Space Person

| Action | Method | Description |
| --- | --- | --- |
| [Get People Currently in Space](actions/get-people-currently-in-space.md) | GET |  |

