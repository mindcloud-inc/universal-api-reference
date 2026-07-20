# Socket: Get Quota

Retrieves current API quota details from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-quota
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-quota?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-quota?${params}`, {
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
      "maxQuota": 1,
      "nextWindowRefresh": "string",
      "quota": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `maxQuota` | number |  |
| `nextWindowRefresh` | string |  |
| `quota` | number |  |

## Native endpoint

Through the native Socket API, this operation is `GET /quota` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quota.md) for the provider-specific parameters and requirements.

