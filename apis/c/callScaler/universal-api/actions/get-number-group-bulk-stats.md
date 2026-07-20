# CallScaler: Get Number Group Bulk Stats

Retrieves number group bulk stats from CallScaler.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-number-group-bulk-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-number-group-bulk-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-number-group-bulk-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "stats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stats` | object | Bulk number-group statistics keyed by group. |

## Native endpoint

Through the native CallScaler API, this operation is `GET /number-groups/bulk-stats` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-number-group-bulk-stats.md) for the provider-specific parameters and requirements.

