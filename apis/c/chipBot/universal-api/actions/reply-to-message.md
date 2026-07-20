# ChipBot: Reply to Message



```
POST https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/reply-to-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/reply-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/reply-to-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Customer email from the incoming chat message webhook payload. |
| `message` | string | yes | Reply content to send back to the thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Reply result payload. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `POST /api/v2/connect/accounts/:accountId/domains/:domainId/messages` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-message.md) for the provider-specific parameters and requirements.

