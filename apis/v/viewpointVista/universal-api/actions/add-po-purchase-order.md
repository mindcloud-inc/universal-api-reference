# Viewpoint Vista: Add PO Purchase Order

Adds a Purchase Order

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-po-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-po-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "2026-05-01",
  "BatchId": 1,
  "PO": "string",
  "Vendor": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-po-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "2026-05-01",
    "BatchId": 1,
    "PO": "string",
    "Vendor": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | Vista PR company. |
| `mth` | string | yes | Posting month for the batch. Format: YYYY-MM-DD. Example: `2026-05-01`. |
| `BatchId` | number | yes |  |
| `PO` | string | yes |  |
| `Vendor` | number | yes |  |
| `Description` | string | no |  |
| `OrderDate` | string | no |  |
| `OrderedBy` | string | no |  |
| `ExpDate` | string | no |  |
| `Status` | number | no | Options: 0-Open, 1-Complete, 2-Close. Optional. If omitted, 0 will be defaulted. |
| `JCCo` | number | no |  |
| `Job` | string | no |  |
| `INCo` | number | no |  |
| `Loc` | string | no |  |
| `ShipLoc` | string | no |  |
| `ShipAddress` | object | no |  |
| `PayTerms` | string | no |  |
| `Notes` | string | no |  |
| `WorkOrder` | number | no |  |
| `__custom_fields` | object | no |  |
| `LineItems[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "operation": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `operation` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/po/2/data/po_batch_entries/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-po-purchase-order.md) for the provider-specific parameters and requirements.

