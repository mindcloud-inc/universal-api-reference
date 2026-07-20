# Eventzilla: Get User

Retrieves a user from Eventzilla.

```
GET https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | The Eventzilla user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user` | array<object> |  |

## Native endpoint

Through the native Eventzilla API, this operation is `GET /users/:userid` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

