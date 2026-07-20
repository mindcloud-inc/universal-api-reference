# Greip - Fraud Prevention: Get IP Reputation

Retrieves IP reputation data from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-reputation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-reputation?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-reputation?${params}`, {
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
| `ip` | string | yes | The IPv4 or IPv6 address to check for reputation and threat indicators. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ip": "string",
      "threats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ip` | string |  |
| `threats` | object |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /lookup/ip/threats` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-reputation.md) for the provider-specific parameters and requirements.

