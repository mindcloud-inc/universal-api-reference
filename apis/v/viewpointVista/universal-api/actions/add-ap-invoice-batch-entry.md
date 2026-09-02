# Viewpoint Vista: Add AP Invoice Batch Entry



```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ap-invoice-batch-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ap-invoice-batch-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "2026-09-01",
  "batchId": 1,
  "vendor": 1,
  "apRef": "string",
  "invDate": "2026-09-01",
  "lineItems[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ap-invoice-batch-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "2026-09-01",
    "batchId": 1,
    "vendor": 1,
    "apRef": "string",
    "invDate": "2026-09-01",
    "lineItems[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | AP company. Allowed range: 1 to 255. |
| `mth` | string | yes | Invoice batch posting month. Format: YYYY-MM-01. Example: `2026-09-01`. |
| `batchId` | number | yes | Invoice batch ID. Key to ap/inv_batches(Co, Mth, BatchId). |
| `vendor` | number | yes | Vendor ID. The vendor group defaults from Co. |
| `apRef` | string | yes | Invoice number. Maximum 30 characters. |
| `description` | string | no | Optional invoice description. Maximum 30 characters. |
| `invDate` | string | yes | Invoice date. Format: YYYY-MM-DD. Example: `2026-09-01`. |
| `notes` | string | no | Optional invoice notes. |
| `lineItems[]` | array<object> | yes | Required array with at least one AP line item object. Each item must use one supported Trimble LineType (1 through 8) and its documented fields. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `discDate` | string | no | Optional discount date. Format: YYYY-MM-DD. Example: `2026-09-01`. |
| `dueDate` | string | no | Optional due date. Defaults from the vendor's payment terms when omitted. Format: YYYY-MM-DD. Example: `2026-09-01`. |
| `invTotal` | string | no | Optional invoice total. When omitted, Trimble calculates it from the line items. |
| `paymentOverride` | object | no | Optional payment override object. Use the documented PaymentOverride fields. |
| `addressOverride` | object | no | Optional address override object. Use the documented AddressOverride fields. |
| `__custom_fields` | object | no | Optional Vista user-defined fields, keyed by the Vista field name. |
| `disableValidation` | boolean | no | Optional. Disables Vista validations for this request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ap/2/data/inv_batch_entries/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-ap-invoice-batch-entry.md) for the provider-specific parameters and requirements.

