# DNSFilter: List Networks



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-networks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-networks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-networks?${params}`, {
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
| `search` | string | no | Search among the network name, hostname, IP address, and related values. |
| `protected` | boolean | no | Filter networks with assigned policy. |
| `unprotected` | boolean | no | Filter networks without assigned policy. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `basicInfo` | boolean | no | Return most basic Network Info only. Defaults to false. |
| `countNetworkIps` | boolean | no | Return count of IP Addresses. Defaults to false. |
| `forceTruncateIps` | boolean | no | Return Network info without IP Addresses. Defaults to false. |

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

Through the native DNSFilter API, this operation is `GET /v1/networks` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-networks.md) for the provider-specific parameters and requirements.

