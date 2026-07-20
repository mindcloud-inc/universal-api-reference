# elmah.io: Fix Message

Marks a message as fixed in elmah.io.

```
PUT https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/fix-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/fix-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "logId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/fix-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "logId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logId` | string | yes | The ID of the log containing the message. |
| `id` | string | yes | The ID of the message to fix. |
| `markAllAsFixed` | boolean | no | If true, all instances of the log message are set to fixed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native elmah.io API returns.

## Native endpoint

Through the native elmah.io API, this operation is `POST /v3/messages/:logId/:id/_fix` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fix-message.md) for the provider-specific parameters and requirements.

