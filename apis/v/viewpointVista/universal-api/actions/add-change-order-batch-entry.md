# Viewpoint Vista: Add Change Order Batch Entry



```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-change-order-batch-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-change-order-batch-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "string",
  "batchId": 1,
  "po": "string",
  "poItem": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-change-order-batch-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "string",
    "batchId": 1,
    "po": "string",
    "poItem": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | Company. Key to the change order batch. |
| `mth` | string | yes | Batch posting month in YYYY-MM-01 format. |
| `batchId` | number | yes | Change order batch ID. |
| `po` | string | yes | Purchase order number. |
| `poItem` | number | yes | Purchase order line item number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pocoNum` | number | no | Optional PO change order number; the next available number is used when omitted. |
| `changeOrder` | string | no | Optional change order number used to group related changes. |
| `actDate` | string | no | Optional action date in YYYY-MM-DD format. |
| `description` | string | no | Optional change description. |
| `changeCurUnits` | string | no | Optional change to current units for non-LS items. |
| `changeBOUnits` | string | no | Optional change to backorder units for non-LS items. |
| `changeCurCost` | string | no | Optional change to current cost for LS items. |
| `changeBOCost` | string | no | Optional change to backorder cost for LS items. |
| `newLineItem` | object | no | Optional details used when adding a new PO line item. |
| `notes` | string | no | Optional entry notes. |
| `__custom_fields` | object | no | Optional Vista user-defined fields, keyed by field name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/po/2/data/co_batch_entries/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-change-order-batch-entry.md) for the provider-specific parameters and requirements.

