# CueGrowth: Send Message To Inbox



```
POST https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/send-message-to-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/send-message-to-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/send-message-to-inbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | ID of the inbox. |
| `message` | string | no | Message to send to the inbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "task_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `task_id` | number |  |

## Native endpoint

Through the native CueGrowth API, this operation is `POST /inbox/{inbox_id}/send` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-inbox.md) for the provider-specific parameters and requirements.

