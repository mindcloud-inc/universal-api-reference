# redirect.pizza: Check Domain DNS



```
PUT https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/check-domain-dns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/check-domain-dns" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/check-domain-dns', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the domain to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "dns": {},
      "fqdn": "string",
      "hsts": true,
      "id": 1,
      "isRootDomain": true,
      "preventForeignEmbedding": true,
      "referrerPolicy": "string",
      "ssl": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `dns` | object |  |
| `fqdn` | string |  |
| `hsts` | boolean |  |
| `id` | number |  |
| `isRootDomain` | boolean |  |
| `preventForeignEmbedding` | boolean |  |
| `referrerPolicy` | string |  |
| `ssl` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `POST /api/v1/domains/{id}/check-dns` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain-dns.md) for the provider-specific parameters and requirements.

