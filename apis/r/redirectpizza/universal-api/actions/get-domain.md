# redirect.pizza: Get Domain



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-domain?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-domain?${params}`, {
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
| `id` | number | yes | ID of the domain. |

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

Through the native redirect.pizza API, this operation is `GET /api/v1/domains/{id}` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

