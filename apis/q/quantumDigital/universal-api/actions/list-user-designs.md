# Quantum Digital: List User Designs



```
GET https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-user-designs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-user-designs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-user-designs?${params}`, {
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
      "description": "string",
      "id": "string",
      "lastUsed": "2026-05-07T12:00:00.000Z",
      "prettyService": "string",
      "productTypeName": "Ava Chen",
      "whichSides": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Design description or name. |
| `id` | string | Provider identifier for the design. |
| `lastUsed` | date | Last used timestamp. |
| `prettyService` | string | Human-readable service name. |
| `productTypeName` | string | Product type label. |
| `whichSides` | string | Printable sides summary. |

## Native endpoint

Through the native Quantum Digital API, this operation is `GET /v1/userdesigns` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-designs.md) for the provider-specific parameters and requirements.

