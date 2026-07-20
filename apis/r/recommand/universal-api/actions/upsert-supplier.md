# Recommand: Upsert Supplier

Finds a supplier in Recommand, or creates one if no match is found.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/upsert-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/upsert-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/upsert-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalid` | string | no | The external ID of the supplier. If provided without id, finds by externalId and updates or creates if not found. |
| `id` | string | no | The internal ID of the supplier to update. If provided, updates by id. |
| `name` | string | yes | The name of the supplier |
| `peppoladdresses[]` | array<string> | no | The Peppol addresses of the supplier |
| `vatnumber` | string | no | The VAT number of the supplier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "supplier": {
        "createdAt": "string",
        "externalId": "string",
        "id": "string",
        "labels": [
          {}
        ],
        "name": "Ava Chen",
        "peppolAddresses": [
          "string"
        ],
        "teamId": "string",
        "updatedAt": "string",
        "vatNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `supplier` | object |  |
| `supplier.createdAt` | string |  |
| `supplier.externalId` | string |  |
| `supplier.id` | string |  |
| `supplier.labels` | array<object> |  |
| `supplier.name` | string |  |
| `supplier.peppolAddresses` | array<string> |  |
| `supplier.teamId` | string |  |
| `supplier.updatedAt` | string |  |
| `supplier.vatNumber` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/suppliers` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-supplier.md) for the provider-specific parameters and requirements.

