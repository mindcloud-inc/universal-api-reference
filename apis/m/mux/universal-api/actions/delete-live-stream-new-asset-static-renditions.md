# Mux: Delete Live Stream New Asset Static Renditions



```
DELETE https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-live-stream-new-asset-static-renditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-live-stream-new-asset-static-renditions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-live-stream-new-asset-static-renditions?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Mux API, this operation is `DELETE /video/v1/live-streams/{LIVE_STREAM_ID}/new-asset-settings/static-renditions` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-live-stream-new-asset-static-renditions.md) for the provider-specific parameters and requirements.

