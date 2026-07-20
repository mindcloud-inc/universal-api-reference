# Camio: Update Profile

Updates a profile in Camio.

```
PUT https://connect.mindcloud.co/v1/universal/camio/latest/actions/update-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/camio/latest/actions/update-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/camio/latest/actions/update-profile', {
  method: 'PUT',
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
| `firstName` | string | no | Optional first name for the profile. |
| `lastName` | string | no | Optional last name for the profile. |
| `timezone` | object | no | Optional timezone object, for example `{ "timezone_offset": "-0300" }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "emailAddress": "ava@example.com",
      "timezone": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | The primary email address. |
| `emailAddress` | string | The email alias returned by Camio. |
| `timezone` | object | The updated timezone object. |
| `userId` | string | The Camio user id. |

## Native endpoint

Through the native Camio API, this operation is `POST /users/:user/profile` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-profile.md) for the provider-specific parameters and requirements.

