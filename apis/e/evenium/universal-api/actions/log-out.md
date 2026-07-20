# Evenium: Log Out

Logs out of Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/log-out
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/log-out?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/log-out?${params}`, {
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
| `success` | boolean | Synthetic logout success flag for no-content responses. |

## Native endpoint

Through the native Evenium API, this operation is `GET /logout/` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-out.md) for the provider-specific parameters and requirements.

