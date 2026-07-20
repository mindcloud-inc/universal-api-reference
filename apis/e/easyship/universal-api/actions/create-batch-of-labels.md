# Easyship: Create Batch of Labels

Creates a batch of shipment labels in Easyship.

```
POST https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-batch-of-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-batch-of-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipments[]": [
    {}
  ],
  "shipments[].easyshipShipmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-batch-of-labels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipments[]": [{}],
    "shipments[].easyshipShipmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipments[]` | array<object> | yes | Shipments to confirm and label. |
| `shipments[].easyshipShipmentId` | string | yes | Existing Easyship shipment ID to label. |
| `shipments[].courierServiceId` | string | no | Optional courier service override for this shipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "finishedAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "startedAt": "2026-05-07T12:00:00.000Z",
        "state": "string",
        "type": "string"
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch.createdAt` | date | When the label batch was created. |
| `batch.finishedAt` | date | When Easyship finished processing the batch. |
| `batch.id` | string | The Easyship label batch ID. |
| `batch.startedAt` | date | When Easyship started processing the batch. |
| `batch.state` | string | Current label batch state. |
| `batch.type` | string | Easyship batch type. |
| `meta.requestId` | string | Easyship request identifier. |

## Native endpoint

Through the native Easyship API, this operation is `POST /batches/labels` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-of-labels.md) for the provider-specific parameters and requirements.

