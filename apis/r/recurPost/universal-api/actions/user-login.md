# RecurPost: User Login

Verifies RecurPost API credentials.

```
GET https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/user-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RecurPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/user-login?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/user-login?${params}`, {
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
      "message": "string",
      "status": 1,
      "user_info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |
| `user_info` | object |  |

## Native endpoint

Through the native RecurPost API, this operation is `POST /api/user_login` (base URL `https://social.recurpost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/user-login.md) for the provider-specific parameters and requirements.

