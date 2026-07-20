# Frappe: Login V1

Logs in a user to Frappe.

```
POST https://connect.mindcloud.co/v1/universal/frappe/latest/actions/login-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/login-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frappe/latest/actions/login-v1', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "full_name": "Ava Chen",
      "home_page": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `full_name` | string | Full name for the logged in user. |
| `home_page` | string | Home page route returned after login. |
| `message` | string | Login result from Frappe. |

## Native endpoint

Through the native Frappe API, this operation is `POST /api/method/login` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login-v1.md) for the provider-specific parameters and requirements.

