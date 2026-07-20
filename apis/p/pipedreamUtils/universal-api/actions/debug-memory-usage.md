# Pipedream Utils: Debug Memory Usage

Retrieves workflow memory usage in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/debug-memory-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/debug-memory-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/debug-memory-usage?${params}`, {
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
      "heapSizeLimit": "string",
      "totalAvailableSize": "string",
      "totalHeapSize": "string",
      "totalHeapSizeExecutable": "string",
      "totalPhysicalSize": "string",
      "usedHeapSize": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `heapSizeLimit` | string |  |
| `totalAvailableSize` | string |  |
| `totalHeapSize` | string |  |
| `totalHeapSizeExecutable` | string |  |
| `totalPhysicalSize` | string |  |
| `usedHeapSize` | string |  |

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/debug-memory-usage.md) for the provider-specific parameters and requirements.

