# Gupshup: Mark Message As Read

Marks a message as read in Gupshup.

```
PUT https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/mark-message-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/mark-message-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "msgId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/mark-message-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "msgId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Gupshup app ID. |
| `msgId` | string | yes | Gupshup message ID to mark as read. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Gupshup response message. |
| `status` | string | Read-state update status returned by Gupshup. |

## Native endpoint

Through the native Gupshup API, this operation is `PUT /wa/app/{appId}/msg/{msgId}/read` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-message-as-read.md) for the provider-specific parameters and requirements.

