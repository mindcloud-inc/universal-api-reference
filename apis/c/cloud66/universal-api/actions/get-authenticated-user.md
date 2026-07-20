# Cloud 66: Get Authenticated User

Retrieves the authenticated user from your Cloud 66 account.

```
GET https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-authenticated-user?${params}`, {
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
      "accountId": 1,
      "accountName": "Ava Chen",
      "message": "string",
      "ok": true,
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `accountName` | string |  |
| `message` | string |  |
| `ok` | boolean |  |
| `userId` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native Cloud 66 API, this operation is `GET /ping/auth` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

