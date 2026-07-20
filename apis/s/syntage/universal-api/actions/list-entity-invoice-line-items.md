# Syntage: List Entity Invoice Line Items

Retrieves invoice line items for an entity in Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entity-invoice-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entity-invoice-line-items?connectionId=$CONNECTION_ID&entityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entity-invoice-line-items?${params}`, {
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
| `entityId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@id": "string",
      "@type": "string",
      "description": "string",
      "discountAmount": 1,
      "id": "string",
      "identificationNumber": "string",
      "invoice": {},
      "productIdentification": "string",
      "quantity": 1,
      "retainedTaxes": {},
      "totalAmount": 1,
      "transferredTaxes": {},
      "unitAmount": 1,
      "unitCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `description` | string |  |
| `discountAmount` | number |  |
| `id` | string |  |
| `identificationNumber` | string |  |
| `invoice` | object |  |
| `productIdentification` | string |  |
| `quantity` | number |  |
| `retainedTaxes` | object |  |
| `totalAmount` | number |  |
| `transferredTaxes` | object |  |
| `unitAmount` | number |  |
| `unitCode` | string |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /entities/:entityId/invoices/line-items` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entity-invoice-line-items.md) for the provider-specific parameters and requirements.

