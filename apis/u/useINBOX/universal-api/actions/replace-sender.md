# UseINBOX: Replace Sender

Replaces an existing sender in UseINBOX.

```
PUT https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/replace-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/replace-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "DisplayName": "Ava Chen",
  "Email": "ava@example.com",
  "ReplyEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/replace-sender', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "DisplayName": "Ava Chen",
    "Email": "ava@example.com",
    "ReplyEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Sender ID from INBOX. |
| `DisplayName` | string | yes | Sender display name. |
| `Email` | string | yes | Sender email address. |
| `ReplyEmail` | string | yes | Reply-to email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string",
      "replyEmail": "ava@example.com",
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date |  |
| `displayName` | string |  |
| `email` | string |  |
| `id` | string |  |
| `replyEmail` | string |  |
| `updateTime` | date |  |

## Native endpoint

Through the native UseINBOX API, this operation is `PUT /inbox/v1/senders/:id` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-sender.md) for the provider-specific parameters and requirements.

