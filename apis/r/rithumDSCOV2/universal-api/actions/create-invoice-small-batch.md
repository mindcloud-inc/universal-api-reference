# Rithum DSCO: Create Invoice Small Batch



```
POST https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/create-invoice-small-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/create-invoice-small-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoices[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/create-invoice-small-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoices[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoices[]` | array<object> | yes | Array of invoice objects to create in one small batch request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventDate": "2026-05-07T12:00:00.000Z",
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventDate` | date | Timestamp of the batch request. |
| `requestId` | string | DSCO request ID for the small batch invoice request. |
| `status` | string | Invoice batch creation status. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `POST invoice/batch/small` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice-small-batch.md) for the provider-specific parameters and requirements.

