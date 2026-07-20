# Frappe: Get Logged User V1 Alias

Retrieves the logged-in user from Frappe.

```
GET https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-logged-user-v1-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-logged-user-v1-alias?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-logged-user-v1-alias?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | The username tied to the authenticated request. |

## Native endpoint

Through the native Frappe API, this operation is `GET /api/v1/method/frappe.auth.get_logged_user` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-logged-user-v1-alias.md) for the provider-specific parameters and requirements.

