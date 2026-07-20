# Instabot: Update User

Updates an existing user in Instabot.

```
PUT https://connect.mindcloud.co/v1/universal/instabot/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instabot/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Instabot user object identifier. |
| `username` | string | yes | Unique user name. |
| `name` | string | no | User display name. |
| `description` | string | no | User description. |
| `email` | string | no | User email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiStatusCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiStatusCode` | string |  |

## Native endpoint

Through the native Instabot API, this operation is `PUT /users/:id` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

