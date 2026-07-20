# Pushbullet: Get Current User

Retrieves the current user from Pushbullet.

```
GET https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": 1,
      "email": "ava@example.com",
      "emailNormalized": "ava@example.com",
      "iden": "string",
      "imageUrl": "https://example.com",
      "maxUploadSize": 1,
      "modified": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | number |  |
| `email` | string |  |
| `emailNormalized` | string |  |
| `iden` | string |  |
| `imageUrl` | string |  |
| `maxUploadSize` | number |  |
| `modified` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `GET /users/me` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

