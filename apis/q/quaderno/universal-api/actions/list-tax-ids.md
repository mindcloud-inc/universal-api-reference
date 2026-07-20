# Quaderno: List Tax IDs

Retrieves registered tax IDs from Quaderno.

```
GET https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-tax-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-tax-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-tax-ids?${params}`, {
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
      "createdAt": 1,
      "id": 1,
      "importScheme": true,
      "jurisdiction": {
        "country": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "permanentEstablishment": true,
      "state": "string",
      "validFrom": "string",
      "validUntil": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `id` | number |  |
| `importScheme` | boolean |  |
| `jurisdiction.country` | string |  |
| `jurisdiction.id` | number |  |
| `jurisdiction.name` | string |  |
| `permanentEstablishment` | boolean |  |
| `state` | string |  |
| `validFrom` | string |  |
| `validUntil` | object |  |
| `value` | string |  |

## Native endpoint

Through the native Quaderno API, this operation is `GET /tax_ids` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tax-ids.md) for the provider-specific parameters and requirements.

