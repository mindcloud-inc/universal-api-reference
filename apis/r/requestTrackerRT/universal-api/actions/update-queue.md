# Request Tracker (RT): Update Queue

Updates an existing queue in Request Tracker.

```
PUT https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/update-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/update-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "queueId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/update-queue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "queueId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Updated queue description. |
| `name` | string | no | Updated queue name. |
| `queueId` | string | yes | The RT queue ID or queue name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `disabled` | boolean | no | Set to true to disable the queue. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "queueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `queueId` | string | Updated queue identifier returned by the wrapper fallback when RT returns an empty body. |

## Native endpoint

Through the native Request Tracker (RT) API, this operation is `PUT queue/:queueId` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-queue.md) for the provider-specific parameters and requirements.

