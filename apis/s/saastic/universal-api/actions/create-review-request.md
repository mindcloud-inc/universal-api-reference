# Saastic: Create Review Request

Creates a review request in Saastic.

```
POST https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-review-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saastic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-review-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-review-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | The customer's email address. Required when phone is not provided. |
| `phone` | string | no | The customer's phone number. Required when email is not provided. |
| `channels[]` | array<string> | no | Include email, sms, or both channels. |
| `remindersCount` | number | no | Number of reminders to send, from 0 to 3. |
| `askedAt` | date | no | The date to schedule the request. If null, it sends immediately. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "phone": "string",
      "scheduled_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `phone` | string |  |
| `scheduled_at` | date |  |

## Native endpoint

Through the native Saastic API, this operation is `POST /beacon/asks` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-review-request.md) for the provider-specific parameters and requirements.

