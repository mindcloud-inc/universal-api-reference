# Nango: Get Sync Status



```
GET https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-sync-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nango `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-sync-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-sync-status?${params}`, {
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
      "syncs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `syncs` | array<object> |  |

## Native endpoint

Through the native Nango API, this operation is `GET /sync/status` (base URL `https://api.nango.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sync-status.md) for the provider-specific parameters and requirements.

