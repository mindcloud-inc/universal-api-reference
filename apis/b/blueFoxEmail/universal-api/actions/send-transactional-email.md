# BlueFox Email: Send Transactional Email

Sends a transactional email through BlueFox Email.

```
POST https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/send-transactional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueFox Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/send-transactional-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "transactionalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/send-transactional-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "transactionalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string<string> | yes | Recipient email address for the transactional email. |
| `transactionalId` | string | yes | BlueFox transactional email ID. |

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
| `success` | boolean |  |

## Native endpoint

Through the native BlueFox Email API, this operation is `POST /v1/send-transactional` (base URL `https://api.bluefox.email`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-email.md) for the provider-specific parameters and requirements.

