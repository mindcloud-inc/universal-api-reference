# Tiliter: Create Transaction Events Batch

Creates transaction events in Tiliter in a batch.

```
POST https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-transaction-events-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-transaction-events-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionEvents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-transaction-events-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionEvents[]": [{}],
    "transactionEvents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionEvents[]` | array<object> | yes |  |
| `transactionEvents[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "reason": "string",
          "recognitionId": "string",
          "result": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].reason` | string |  |
| `data[].recognitionId` | string |  |
| `data[].result` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `POST /recognition/transaction_events/batch` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction-events-batch.md) for the provider-specific parameters and requirements.

