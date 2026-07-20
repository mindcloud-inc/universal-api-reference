# DNSFilter: Lookup Domain



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/lookup-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/lookup-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/lookup-domain?${params}`, {
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
| `fqdn` | string | no | FQDN to lookup |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "category": "string",
      "id": "string",
      "name": "Ava Chen",
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
| `category` | string |  |
| `id` | string |  |
| `name` | string |  |
| `relationships` | object |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/domains/user_lookup` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-domain.md) for the provider-specific parameters and requirements.

