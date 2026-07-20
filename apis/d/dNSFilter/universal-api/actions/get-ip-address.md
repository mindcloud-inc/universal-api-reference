# DNSFilter: Get IP Address



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-ip-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-ip-address?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-ip-address?${params}`, {
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
| `id` | number | yes | IP address ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `relationships` | object |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/ip_addresses/:id` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-address.md) for the provider-specific parameters and requirements.

