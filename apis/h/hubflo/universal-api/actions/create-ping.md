# Hubflo: Create Ping

Checks Hubflo API authentication with a ping.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-ping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-ping?${params}`, {
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
      "pong": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pong` | string | Connectivity check response from Hubflo. |

## Native endpoint

Through the native Hubflo API, this operation is `POST /pings` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ping.md) for the provider-specific parameters and requirements.

