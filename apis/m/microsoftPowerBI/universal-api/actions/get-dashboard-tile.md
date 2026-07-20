# Microsoft Power BI: Get Dashboard Tile



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-dashboard-tile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-dashboard-tile?connectionId=$CONNECTION_ID&groupId=string&dashboardId=string&tileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "dashboardId": "string",
  "tileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-dashboard-tile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace ID. |
| `dashboardId` | string | yes | The dashboard ID. |
| `tileId` | string | yes | The tile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colSpan": 1,
      "datasetId": "string",
      "embedData": "string",
      "embedUrl": "https://example.com",
      "id": "string",
      "reportId": "string",
      "rowSpan": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colSpan` | number | The tile column span. |
| `datasetId` | string | The dataset ID associated with the tile. |
| `embedData` | string | Additional embed data for the tile. |
| `embedUrl` | string | The embed URL of the tile. |
| `id` | string | The tile ID. |
| `reportId` | string | The report ID associated with the tile. |
| `rowSpan` | number | The tile row span. |
| `title` | string | The tile title. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/dashboards/[:dashboardId]/tiles/[:tileId]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard-tile.md) for the provider-specific parameters and requirements.

