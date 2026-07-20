# JmpTo: Get Account

Retrieves account details from JmpTo.

```
GET https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-account?${params}`, {
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
      "avatar": "string",
      "email": "ava@example.com",
      "expires": "string",
      "id": 1,
      "planid": 1,
      "registered": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | Avatar URL. |
| `email` | string | Account email address. |
| `expires` | string | Plan expiration value. |
| `id` | number | Account ID. |
| `planid` | number | Plan ID. |
| `registered` | string | Registration timestamp. |
| `status` | string | Account plan/status. |
| `username` | string | Account username. |

## Native endpoint

Through the native JmpTo API, this operation is `GET /account` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

