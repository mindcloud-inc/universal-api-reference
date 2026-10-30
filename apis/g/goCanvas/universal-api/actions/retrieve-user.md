# GoCanvas: Retrieve User



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-user?${params}`, {
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
| `userId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "createdAt": "string",
      "enabled": true,
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "login": "string",
      "phone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `createdAt` | string |  |
| `enabled` | boolean |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `login` | string |  |
| `phone` | string |  |
| `type` | string |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /users/:userId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

