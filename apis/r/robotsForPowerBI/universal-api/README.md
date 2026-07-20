# <img src="https://images.mindcloud.co/apps/icons/robots-for-power-bi_1777544799404.png" alt="Robots for Power BI logo" width="28" height="28"> Robots for Power BI: Universal API

Automate PowerBI Robots playlist operations from MindCloud, including enabling, disabling, and executing playlists through the PowerBI Robots public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/robotsForPowerBI/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://powerbitiles.com/PowerBIRobots
- **Vendor API docs:** https://docs.pbirobots.powerbitiles.com/guides/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Disable playlist](actions/disable-playlist.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/robotsForPowerBI/latest/actions/disable-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "00000000-0000-0000-0000-000000000000"
}'
```

## Actions (3)

### Playlist

| Action | Method | Description |
| --- | --- | --- |
| [Disable playlist](actions/disable-playlist.md) | PUT | Disables a playlist in Robots for Power BI. |
| [Enable playlist](actions/enable-playlist.md) | PUT | Enables a playlist in Robots for Power BI. |

### Playlist Execution

| Action | Method | Description |
| --- | --- | --- |
| [Execute playlist](actions/execute-playlist.md) | POST | Executes a playlist in Robots for Power BI. |

