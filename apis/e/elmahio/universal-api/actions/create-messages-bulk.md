# elmah.io: Create Messages Bulk

Creates one or more messages in elmah.io.

```
POST https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-messages-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-messages-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "logId": "string",
  "messages[]": [
    {}
  ],
  "messages[].title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-messages-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "logId": "string",
    "messages[]": [{}],
    "messages[].title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logId` | string | yes | The ID of the log which should contain the new messages. |
| `messages[]` | array<object> | yes | The messages to create. |
| `messages[].title` | string | yes | The textual title or headline of each message to log. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location` | string | Location of the created message when the bulk item succeeds. |
| `statusCode` | number | Status code for the individual bulk-created message. |

## Native endpoint

Through the native elmah.io API, this operation is `POST /v3/messages/:logId/_bulk` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-messages-bulk.md) for the provider-specific parameters and requirements.

