# Rillion Prime Web Service: Insert Item

Insert a purchasing item into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "item": {},
  "item.item": "string",
  "item.supplier": "string",
  "item.description": "string",
  "item.href": "string",
  "item.priceFromDate": "2026-05-07T12:00:00.000Z",
  "item.currency": "string",
  "item.price": 1,
  "item.discount": 1,
  "item.tax": 1,
  "item.tagWords": "string",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "item": {},
    "item.item": "string",
    "item.supplier": "string",
    "item.description": "string",
    "item.href": "string",
    "item.priceFromDate": "2026-05-07T12:00:00.000Z",
    "item.currency": "string",
    "item.price": 1,
    "item.discount": 1,
    "item.tax": 1,
    "item.tagWords": "string",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Item section. |
| `item.item` | string | yes | Item number |
| `item.supplier` | string | yes | Supplier |
| `item.description` | string | yes | Description |
| `item.href` | string | yes |  |
| `item.priceFromDate` | date | yes | Price valid from this date |
| `item.currency` | string | yes | Currency |
| `item.price` | number | yes | Price (gross) |
| `item.discount` | number | yes | Discount in % |
| `item.tax` | number | yes | Tax or additional costs |
| `item.tagWords` | string | yes |  |
| `itemImage` | object | no | Optional image payload for the item. |
| `itemAttachment` | object | no | Optional attachment payload for the item. |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item.itemFormName` | string | no |  |
| `item.company` | list<string> | no | Company for the intem |
| `item.commodity` | string | no | Commodity |
| `item.note` | string | no | Detailed description |
| `item.supplierItem` | string | no | Item number from the supplier |
| `item.manufacturer` | string | no | Name of manufacture |
| `item.manufacturerItem` | string | no | Item number from the manufacture |
| `item.blocked` | string | no | Blocked for purchase: 0=No; 1=Yes |
| `item.validFrom` | date | no | Item availbable from this date |
| `item.validTo` | date | no | Item availbable to this date |
| `item.daysOfDelivery` | number | no | Delivery term in days (0-366) |
| `item.responsiblePurchaseOrderRole` | string | no | Responsible purchaser |
| `item.account` | string | no | Default expenditure account |
| `item.imageFile` | string | no | Filename of the image for the item |
| `item.imageHref` | string | no | Url or file reference to image or other document for more details of the item |
| `item.bestBuy` | string | no |  |
| `item.commodityCode` | string | no | Commodity code |
| `item.fileTypeID` | number | no | File type ID set up in Prime Master |
| `item.attachedFile` | string | no | Filename for import of image to the item |
| `item.unit` | string | no | Unit |
| `item.group1` | string | no | Free field of Type 1 |
| `item.group2` | string | no | Free field of Type 2 |
| `item.group3` | string | no | Free field of Type 3 |
| `item.keyType` | boolean | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `item.unitNumber` | number | no | Packaging numbers |
| `item.minNumber` | number | no | Minumum number for ordering |
| `item.minExtraNumber` | number | no | Minumum number of additional order |
| `item.ecoLabel` | string | no | Marked as ecolabelled: 0=No; 1=Yes |
| `item.ecoLabelText` | string | no | Type of EcoLabelling |
| `item.dangerousLabel` | string | no | Marked as dangerous goods: 0=No; 1=Yes |
| `item.dangerousLabelText` | string | no | Type of dangerous goods |
| `item.contractNo` | string | no |  |
| `item.externalId` | string | no |  |
| `item.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-item.md) for the provider-specific parameters and requirements.

