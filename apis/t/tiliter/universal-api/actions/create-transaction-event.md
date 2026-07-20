# Tiliter: Create Transaction Event

Creates a transaction event in the Tiliter Recognition API.

```
POST https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-transaction-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-transaction-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recognitionId": "string",
  "type": "string",
  "time": "2026-05-07T12:00:00.000Z",
  "detail": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-transaction-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recognitionId": "string",
    "type": "string",
    "time": "2026-05-07T12:00:00.000Z",
    "detail": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionId` | string | yes |  |
| `type` | string | yes |  |
| `time` | date | yes |  |
| `detail` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "transactionEventId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |
| `time` | date |  |
| `transactionEventId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `POST /recognition/:recognition_id/transaction_events` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction-event.md) for the provider-specific parameters and requirements.

