# Vimeo: Get User

Retrieves a user record from Vimeo.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=152184" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "152184"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | The ID of the user. Example: `152184`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "bio": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com",
      "name": "Ava Chen",
      "pictures": {},
      "uri": "string",
      "websites": [
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
| `account` | string | Vimeo account tier. |
| `bio` | string | User biography. |
| `createdTime` | date | User creation time. |
| `link` | string | User profile link. |
| `name` | string | User display name. |
| `pictures` | object | User profile pictures. |
| `uri` | string | User URI. |
| `websites` | array<object> | Linked websites. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /users/:user_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

