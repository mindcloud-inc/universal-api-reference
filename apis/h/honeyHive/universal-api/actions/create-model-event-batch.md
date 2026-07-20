# HoneyHive: Create Model Event Batch

Creates a batch of model events in HoneyHive.

```
POST https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-model-event-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-model-event-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelEvents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-model-event-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelEvents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelEvents[]` | array<object> | yes | Model events to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventIds": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventIds` | array<string> |  |
| `success` | boolean |  |

## Native endpoint

Through the native HoneyHive API, this operation is `POST /events/model/batch` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-model-event-batch.md) for the provider-specific parameters and requirements.

