# TikHub: Get TikHub User Info

Retrieves the current TikHub user info.

```
GET https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-tik-hub-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-tik-hub-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-tik-hub-user-info?${params}`, {
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
      "apiKeyData": {
        "apiKeyName": "Ava Chen",
        "apiKeyScopes": [
          "string"
        ],
        "apiKeyStatus": 1,
        "createdAt": "2026-05-07T12:00:00.000Z"
      },
      "code": 1,
      "router": "string",
      "userData": {
        "accountDisabled": true,
        "balance": 1,
        "email": "ava@example.com",
        "emailVerified": true,
        "freeCredit": 1,
        "isActive": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyData.apiKeyName` | string |  |
| `apiKeyData.apiKeyScopes[]` | string |  |
| `apiKeyData.apiKeyStatus` | number |  |
| `apiKeyData.createdAt` | date |  |
| `code` | number |  |
| `router` | string |  |
| `userData.accountDisabled` | boolean |  |
| `userData.balance` | number |  |
| `userData.email` | string |  |
| `userData.emailVerified` | boolean |  |
| `userData.freeCredit` | number |  |
| `userData.isActive` | boolean |  |

## Native endpoint

Through the native TikHub API, this operation is `GET /api/v1/tikhub/user/get_user_info` (base URL `https://api.tikhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tik-hub-user-info.md) for the provider-specific parameters and requirements.

