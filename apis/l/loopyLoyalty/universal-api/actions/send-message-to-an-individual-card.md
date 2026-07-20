# Loopy Loyalty: Send Message To An Individual Card



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/send-message-to-an-individual-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/send-message-to-an-individual-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": "RDX5AsgKYa3UZ7",
  "message": "Thanks for joining our loyalty program."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/send-message-to-an-individual-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": "RDX5AsgKYa3UZ7",
    "message": "Thanks for joining our loyalty program."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | string | yes | Example: `RDX5AsgKYa3UZ7`. |
| `message` | string | yes | Example: `Thanks for joining our loyalty program.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the message was sent successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /card/push` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-an-individual-card.md) for the provider-specific parameters and requirements.

