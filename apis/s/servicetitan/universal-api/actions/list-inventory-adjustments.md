# ServiceTitan: List Inventory Adjustments

Retrieves inventory adjustments from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-inventory-adjustments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-inventory-adjustments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-inventory-adjustments?${params}`, {
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
| `modifiedOnOrAfter` | string | no | Return items modified on or after certain date/time (in UTC) |
| `sort` | string | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order. Available fields are: Id, ModifiedOn, CreatedOn. |
| `syncStatuses` | string | no | Filter by a collection of sync statues |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "batch": {
        "id": 1,
        "name": "Ava Chen",
        "number": "string"
      },
      "batchId": 1,
      "businessUnitId": 1,
      "canceledById": {},
      "canceledReason": {},
      "createdById": 1,
      "createdOn": "string",
      "customFields": {},
      "date": "string",
      "dateCanceled": {},
      "externalData": {},
      "id": 1,
      "inventoryLocationId": 1,
      "items": [
        {
          "active": true,
          "code": "string",
          "createdById": 1,
          "createdOn": "string",
          "description": "string",
          "id": 1,
          "modifiedOn": "string",
          "name": "Ava Chen",
          "quantity": 1,
          "serialNumbers": {},
          "skuId": 1
        }
      ],
      "memo": {},
      "modifiedOn": "string",
      "number": "string",
      "referenceNumber": {},
      "syncStatus": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `batch.id` | number |  |
| `batch.name` | string |  |
| `batch.number` | string |  |
| `batchId` | number |  |
| `businessUnitId` | number |  |
| `canceledById` | object |  |
| `canceledReason` | object |  |
| `createdById` | number |  |
| `createdOn` | string |  |
| `customFields` | object |  |
| `date` | string |  |
| `dateCanceled` | object |  |
| `externalData` | object |  |
| `id` | number |  |
| `inventoryLocationId` | number |  |
| `items[].active` | boolean |  |
| `items[].code` | string |  |
| `items[].createdById` | number |  |
| `items[].createdOn` | string |  |
| `items[].description` | string |  |
| `items[].id` | number |  |
| `items[].modifiedOn` | string |  |
| `items[].name` | string |  |
| `items[].quantity` | number |  |
| `items[].serialNumbers` | object |  |
| `items[].skuId` | number |  |
| `memo` | object |  |
| `modifiedOn` | string |  |
| `number` | string |  |
| `referenceNumber` | object |  |
| `syncStatus` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET inventory/v2/tenant/{{credentials.tenant}}/adjustments` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inventory-adjustments.md) for the provider-specific parameters and requirements.

