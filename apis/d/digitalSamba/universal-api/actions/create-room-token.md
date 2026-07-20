# Digital Samba: Create room token

Creates a room access token in Digital Samba.

```
POST https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-room-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-room-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/create-room-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room` | string | yes | Room path parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON request body documented for this endpoint. |
| `ud` | string | no | External user identifier. |
| `u` | string | no | User name. |
| `initials` | string | no | Custom initials for user tiles. |
| `role` | string | no | Role ID or name. |
| `breakoutId` | string | no | Breakout room id. |
| `avatar` | string | no | The url of the user’s avatar image. |
| `nbf` | number | no | Not before. Unix timestamp before which token is not valid. You can also use a string date time. |
| `exp` | number | no | Token expiration. Unix timestamp after which token is not valid. You can also use number of minutes until token expiration, or a string date time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `POST /rooms/:room/token` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-room-token.md) for the provider-specific parameters and requirements.

