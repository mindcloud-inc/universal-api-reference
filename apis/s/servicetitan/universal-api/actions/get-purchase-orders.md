# ServiceTitan: Get Purchase Orders



```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-purchase-orders?${params}`, {
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
| `modifiedOnOrAfter` | string | no |  |
| `number` | string | no |  |
| `status` | string | no |  |
| `ids` | string | no |  |
| `jobIds` | string | no |  |
| `createdOnOrAfter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": {},
      "budgetCodeId": {},
      "businessUnitId": 1,
      "createdById": 1,
      "createdOn": "string",
      "customFields": [
        [
          {}
        ]
      ],
      "date": "string",
      "id": 1,
      "inventoryLocationId": 1,
      "invoiceId": 1,
      "items": [
        [
          {}
        ]
      ],
      "jobId": 1,
      "modifiedOn": "string",
      "number": "string",
      "projectId": 1,
      "receivedOn": "string",
      "requiredOn": "string",
      "sentOn": "string",
      "shipping": 1,
      "shipTo": {
        "city": "string",
        "country": "string",
        "state": "string",
        "street": "string",
        "unit": {},
        "zip": "string"
      },
      "status": "string",
      "summary": "string",
      "tax": 1,
      "technicianId": 1,
      "total": 1,
      "typeId": 1,
      "vendorDocumentNumber": "string",
      "vendorId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | object |  |
| `budgetCodeId` | object |  |
| `businessUnitId` | number |  |
| `createdById` | number |  |
| `createdOn` | string |  |
| `customFields[]` | array<object> |  |
| `customFields[].name` | string |  |
| `customFields[].typeId` | number |  |
| `customFields[].value` | string |  |
| `date` | string |  |
| `id` | number |  |
| `inventoryLocationId` | number |  |
| `invoiceId` | number |  |
| `items[]` | array<object> |  |
| `items[].budgetCodeId` | object |  |
| `items[].chargeable` | boolean |  |
| `items[].cost` | number |  |
| `items[].createdOn` | string |  |
| `items[].description` | string |  |
| `items[].id` | number |  |
| `items[].modifiedOn` | string |  |
| `items[].quantity` | number |  |
| `items[].quantityReceived` | number |  |
| `items[].serialNumbers` | object |  |
| `items[].skuCode` | string |  |
| `items[].skuId` | number |  |
| `items[].skuName` | string |  |
| `items[].skuType` | string |  |
| `items[].status` | string |  |
| `items[].total` | number |  |
| `items[].vendorPartNumber` | string |  |
| `jobId` | number |  |
| `modifiedOn` | string |  |
| `number` | string |  |
| `projectId` | number |  |
| `receivedOn` | string |  |
| `requiredOn` | string |  |
| `sentOn` | string |  |
| `shipping` | number |  |
| `shipTo` | object |  |
| `shipTo.city` | string |  |
| `shipTo.country` | string |  |
| `shipTo.state` | string |  |
| `shipTo.street` | string |  |
| `shipTo.unit` | object |  |
| `shipTo.zip` | string |  |
| `status` | string |  |
| `summary` | string |  |
| `tax` | number |  |
| `technicianId` | number |  |
| `total` | number |  |
| `typeId` | number |  |
| `vendorDocumentNumber` | string |  |
| `vendorId` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET inventory/v2/tenant/{{credentials.tenant}}/purchase-orders` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-purchase-orders.md) for the provider-specific parameters and requirements.

