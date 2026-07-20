# Product Fruits: Identify User



```
PUT https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/identify-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/identify-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user.username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/identify-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user.username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.firstname` | string | no | First name of the tracked user. |
| `user.lastname` | string | no | Last name of the tracked user. |
| `user.role` | string | no | Role of the tracked user. |
| `user.signUpAt` | date | no | Signup timestamp in JSON date or datetime format. |
| `user.username` | string | yes | Unique username of the tracked user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {
        "firstname": "Ava",
        "lastname": "Chen",
        "props": {},
        "role": "string",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.firstname` | string |  |
| `user.lastname` | string |  |
| `user.props` | object |  |
| `user.role` | string |  |
| `user.username` | string |  |

## Native endpoint

Through the native Product Fruits API, this operation is `POST /v1/identify` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-user.md) for the provider-specific parameters and requirements.

