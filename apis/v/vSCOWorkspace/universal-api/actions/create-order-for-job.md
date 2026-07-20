# VSCO Workspace: Create Order for Job

Creates a new order for a job in VSCO Workspace.

```
POST https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-order-for-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-order-for-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-order-for-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes |  |
| `recipientId` | string | no | A ULID entity identifier that is nullable. |
| `dueDate` | object | no |  |
| `name` | string | no |  |
| `bookedOn` | object | no |  |
| `balance` | object | no |  |
| `lineItems[]` | array<object> | no |  |
| `taxGroupId` | string | no | A ULID entity identifier that is nullable. |
| `taxCombined` | object | no |  |
| `total` | object | no |  |
| `paymentTermsId` | string | no | A ULID entity identifier that is nullable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "afterTaxDiscount": {},
      "balance": {},
      "bookedElectronically": true,
      "bookedFromQuote": true,
      "bookedOn": {},
      "created": "2026-05-07T12:00:00.000Z",
      "customNumber": "string",
      "dueDate": {},
      "hidden": true,
      "id": "string",
      "invoices": [
        {}
      ],
      "jobId": "string",
      "lineItems": [
        {}
      ],
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "paymentAllocations": [
        {}
      ],
      "paymentTermsId": "string",
      "paymentTermsName": "Ava Chen",
      "preTaxDiscount": {},
      "recipientId": "string",
      "referenceCode": "string",
      "status": "string",
      "subtotal": {},
      "tax1": {},
      "tax2": {},
      "tax3": {},
      "taxCombined": {},
      "taxGroupId": "string",
      "taxIsCompounding": true,
      "title": "string",
      "total": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `afterTaxDiscount` | object |  |
| `balance` | object |  |
| `bookedElectronically` | boolean |  |
| `bookedFromQuote` | boolean |  |
| `bookedOn` | object |  |
| `created` | date | A server timestamp (always in UTC) |
| `customNumber` | string |  |
| `dueDate` | object |  |
| `hidden` | boolean | Whether or not the object is hidden. |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `invoices` | array<object> |  |
| `jobId` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `lineItems` | array<object> |  |
| `modified` | date | A server timestamp (always in UTC) |
| `name` | string |  |
| `paymentAllocations` | array<object> |  |
| `paymentTermsId` | string | A ULID entity identifier that is nullable. |
| `paymentTermsName` | string |  |
| `preTaxDiscount` | object |  |
| `recipientId` | string | A ULID entity identifier that is nullable. |
| `referenceCode` | string |  |
| `status` | string |  |
| `subtotal` | object |  |
| `tax1` | object | These values are computed when a taxGroupId is set on the order |
| `tax2` | object | These values are computed when a taxGroupId is set on the order |
| `tax3` | object | These values are computed when a taxGroupId is set on the order |
| `taxCombined` | object |  |
| `taxGroupId` | string | A ULID entity identifier that is nullable. |
| `taxIsCompounding` | boolean | Rarely, certain taxes are compounded one after the other, aka "tax the tax" |
| `title` | string | The name or auto-generated title of the order |
| `total` | object |  |

## Native endpoint

Through the native VSCO Workspace API, this operation is `POST /job/:jobId/order` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-for-job.md) for the provider-specific parameters and requirements.

