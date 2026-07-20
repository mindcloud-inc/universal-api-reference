# Chatrace: List Account Admins

Retrieves account admins from your Chatrace account.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-account-admins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-account-admins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/list-account-admins?${params}`, {
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
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "profile_pic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `profile_pic` | string |  |

## Native endpoint

Through the native Chatrace API, this operation is `GET /accounts/admins` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-admins.md) for the provider-specific parameters and requirements.

