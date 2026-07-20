# Toofr: Queue Email Guess

Queues an email guess in Toofr for callback delivery.

```
POST https://connect.mindcloud.co/v1/universal/toofr/latest/actions/queue-email-guess
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/queue-email-guess" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callbackUrl": "https://example.com",
  "companyName": "Ava Chen",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toofr/latest/actions/queue-email-guess', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callbackUrl": "https://example.com",
    "companyName": "Ava Chen",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | yes | Callback URL for asynchronous email guess result delivery. |
| `companyName` | string | yes | Person company name. |
| `firstName` | string | yes | Person first name. |
| `lastName` | string | yes | Person last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "error": true,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `error` | boolean |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Toofr API, this operation is `POST /guess_email.json` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-email-guess.md) for the provider-specific parameters and requirements.

