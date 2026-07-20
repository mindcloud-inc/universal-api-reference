# Maildrip: Register a new user



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/register-a-new-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/register-a-new-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/register-a-new-user', {
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
| `email` | string | no |  |
| `name` | string | no |  |
| `password` | string | no |  |
| `phone` | string | no |  |
| `companyRole` | string | no |  |
| `companyName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "name": "Ava Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `name` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/users/register` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-a-new-user.md) for the provider-specific parameters and requirements.

