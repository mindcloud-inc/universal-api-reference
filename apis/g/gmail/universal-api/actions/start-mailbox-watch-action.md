# Google Mail: Start Mailbox Watch (Action)

Sets up or updates a Gmail mailbox watch.

```
POST https://connect.mindcloud.co/v1/universal/gmail/latest/actions/start-mailbox-watch-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/start-mailbox-watch-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topicName": "projects/your-project/topics/gmail-updates"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/start-mailbox-watch-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topicName": "projects/your-project/topics/gmail-updates"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topicName` | string | yes | Fully-qualified Pub/Sub topic name (`projects/{project}/topics/{topic}`). Example: `projects/your-project/topics/gmail-updates`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `labelFilterBehavior` | string | no | How labels should be applied when filtering watch notifications (`include` or `exclude`). Default: `INCLUDE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiration": "string",
      "historyId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiration` | string |  |
| `historyId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `POST /watch` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-mailbox-watch-action.md) for the provider-specific parameters and requirements.

