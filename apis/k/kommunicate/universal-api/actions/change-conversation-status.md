# Kommunicate: Change Conversation Status

Updates a conversation status in Kommunicate.

```
PUT https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "status": 1,
  "ofUserId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "status": 1,
    "ofUserId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Conversation identifier to update. |
| `status` | number | yes | Conversation status code: 0 open, 2 close, 3 spam. |
| `sendNotifyMessage` | boolean | no | Whether Kommunicate should send a notification message; defaults to true. |
| `ofUserId` | string | yes | Admin or agent user ID to route into the required Of-User-Id header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generatedAt": 1,
      "response": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generatedAt` | number | Provider-generated timestamp. |
| `response` | string | Provider response message. |
| `status` | string | Provider operation status. |

## Native endpoint

Through the native Kommunicate API, this operation is `PATCH /rest/ws/group/status/change` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-conversation-status.md) for the provider-specific parameters and requirements.

