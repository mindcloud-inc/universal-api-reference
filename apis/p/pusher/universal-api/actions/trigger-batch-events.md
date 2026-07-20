# Pusher: Trigger Batch Events

Triggers multiple events in Pusher.

```
POST https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-batch-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-batch-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batch[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-batch-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batch[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch[]` | array<object> | yes | An array of event objects to publish in a single request, up to 10 events on multi-tenant clusters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch` | array<object> | Returned only when one or more events request channel info. |

## Native endpoint

Through the native Pusher API, this operation is `POST /apps/{{credentials.appId}}/batch_events` (base URL `https://api-{{credentials.cluster}}.pusher.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-batch-events.md) for the provider-specific parameters and requirements.

