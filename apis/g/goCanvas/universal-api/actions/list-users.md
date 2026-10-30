# GoCanvas: List Users



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-users?${params}`, {
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
| `enabled` | boolean | no | Leave unset to return both enabled and disabled users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "address2": "string",
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "enabled": true,
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "login": "string",
      "phone": "string",
      "state": "string",
      "type": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `enabled` | boolean |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `login` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `type` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /users` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

