# Google AI Studio: Cancel Batch

Cancels a batch operation in Google AI Studio.

```
PUT https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/cancel-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "batches/1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/cancel-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "batches/1234567890"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Full batch resource name, for example `batches/1234567890`. Example: `batches/1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Empty object returned by Gemini when batch cancellation is accepted. |

## Native endpoint

Through the native Google AI Studio API, this operation is `POST v1beta/batches/:name` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-batch.md) for the provider-specific parameters and requirements.

