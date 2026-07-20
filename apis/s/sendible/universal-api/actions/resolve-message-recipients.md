# Sendible: Resolve Message Recipients



```
PUT https://connect.mindcloud.co/v1/universal/sendible/latest/actions/resolve-message-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/resolve-message-recipients" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "recipientIds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendible/latest/actions/resolve-message-recipients', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "recipientIds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The Sendible message ID. |
| `recipientIds` | list<number> | yes | Recipient IDs to resolve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
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
| `result` | array<object> |  |

## Native endpoint

Through the native Sendible API, this operation is `POST https://api.prd-tw.sendible.com/v1.0/messages/{{messageId}}/resolve` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-message-recipients.md) for the provider-specific parameters and requirements.

