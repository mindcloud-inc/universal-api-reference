# Giftbit: Ping

Tests your Giftbit authentication and API health.

```
GET https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/ping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/ping?${params}`, {
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
      "displayname": "Ava Chen",
      "info": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayname` | string |  |
| `info` | object |  |
| `username` | string |  |

## Native endpoint

Through the native Giftbit API, this operation is `GET /ping` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping.md) for the provider-specific parameters and requirements.

