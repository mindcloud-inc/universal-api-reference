# SeekTable: Export Dashboard

Exports a SeekTable dashboard in the requested format.

```
GET https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/export-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/export-dashboard?connectionId=$CONNECTION_ID&dashboardId=00f7e942fe7e420694bf478ae659ea58&format=excel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dashboardId": "00f7e942fe7e420694bf478ae659ea58",
  "format": "excel"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/export-dashboard?${params}`, {
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
| `dashboardId` | string | yes | GUID of the dashboard in your SeekTable account. Example: `00f7e942fe7e420694bf478ae659ea58`. |
| `format` | string | yes | Export format for the generated dashboard file. One of: `0`, `1`. Example: `excel`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportParameters` | string | no | JSON object string with report parameter values. Requires Advanced Publishing. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `GET /api/dashboard/:dashboard_id/export` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-dashboard.md) for the provider-specific parameters and requirements.

