# Recommand: Get Supplier

Retrieves a supplier record from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-supplier?connectionId=$CONNECTION_ID&supplierid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supplierid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-supplier?${params}`, {
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
| `supplierid` | string | yes | supplierId parameter. |

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

Through the native Recommand API, this operation is `GET /api/v1/suppliers/:supplierId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier.md) for the provider-specific parameters and requirements.

