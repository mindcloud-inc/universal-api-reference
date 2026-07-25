# Viewpoint Vista: Add Receipt Batch



```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-receipt-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-receipt-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-receipt-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | AR company for the receipt batch. |
| `mth` | string | yes | Posting month for the receipt batch. Format: YYYY-MM-01. |
| `notes` | string | no | Optional notes for the receipt batch. |
| `BatchId` | number | no |  |
| `Customer` | number | no |  |
| `TransDate` | date | no |  |
| `CheckNo` | string | no |  |
| `CheckDate` | date | no |  |
| `CreditAmt` | string | no |  |
| `CMCo` | number | no |  |
| `CMDeposit` | string | no |  |
| `Notes` | string | no |  |
| `__custom_fields` | object | no |  |
| `LineItems[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batches/actions/add_receipt` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-receipt-batch.md) for the provider-specific parameters and requirements.

