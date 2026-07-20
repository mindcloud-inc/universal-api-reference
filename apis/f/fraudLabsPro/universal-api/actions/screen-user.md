# FraudLabs Pro: Screen User

Screens a user for fraud in FraudLabs Pro.

```
POST https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/screen-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/screen-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "ip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/screen-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "ip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The user email address. |
| `ip` | string | yes | The user IP address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reason": [
        [
          "string"
        ]
      ],
      "user_score": 1,
      "user_transaction_id": "string",
      "user_transaction_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason[]` | array<string> | Reasons why the status is REJECT or REVIEW. |
| `user_score` | number | Overall score between 1 and 100. 100 is the highest risk and 1 is the lowest risk. |
| `user_transaction_id` | string | System unique identifier for this user screening transaction. |
| `user_transaction_status` | string | Final action based on the rules analysis. |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `POST v2/user/screen` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/screen-user.md) for the provider-specific parameters and requirements.

