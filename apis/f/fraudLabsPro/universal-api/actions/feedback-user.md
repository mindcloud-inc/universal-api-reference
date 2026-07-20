# FraudLabs Pro: Feedback User

Updates user feedback in FraudLabs Pro.

```
PUT https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "action": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "action": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The FraudLabs Pro user transaction ID or merchant user ID. |
| `action` | string | yes | Feedback action to send. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user_transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user_transaction_id` | string | The User Transaction ID that was updated. |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `POST v2/user/feedback` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/feedback-user.md) for the provider-specific parameters and requirements.

