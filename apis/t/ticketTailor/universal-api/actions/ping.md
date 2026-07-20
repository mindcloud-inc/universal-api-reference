# Ticket Tailor: Ping

Checks if the Ticket Tailor API is responsive.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/ping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/ping?${params}`, {
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
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `version` | string |  |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/ping` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping.md) for the provider-specific parameters and requirements.

