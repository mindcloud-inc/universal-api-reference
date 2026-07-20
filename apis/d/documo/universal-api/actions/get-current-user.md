# Documo: Get Current User

Retrieves current user details from Documo.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/get-current-user?${params}`, {
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
      "account": {
        "accountName": "Ava Chen",
        "accountType": "string",
        "allowApi": true
      },
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "phoneVerified": true,
      "timezone": "string",
      "userRole": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.accountName` | string |  |
| `account.accountType` | string |  |
| `account.allowApi` | boolean |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `phoneVerified` | boolean |  |
| `timezone` | string |  |
| `userRole` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `GET /v1/me` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

