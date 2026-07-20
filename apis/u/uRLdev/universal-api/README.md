# <img src="https://images.mindcloud.co/apps/icons/u-rldev_1777924218604.png" alt="URL.dev logo" width="28" height="28"> URL.dev: Universal API

Use hosted tools through APIs and MCP servers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uRLdev/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://superuser.app
- **Vendor API docs:** https://docs.superuser.app/readme.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Weather](actions/get-current-weather.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uRLdev/latest/actions/get-current-weather?connectionId=$CONNECTION_ID&latitude=37.7749&longitude=-122.4194" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Current Weather

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Weather](actions/get-current-weather.md) | GET | Retrieves current weather for coordinates from URL.dev. |

