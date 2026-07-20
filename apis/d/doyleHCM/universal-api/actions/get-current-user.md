# Doyle HCM: Get current user

Retrieves the current user profile from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-current-user?${params}`, {
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
      "allClientsAccess": true,
      "companies": [
        {}
      ],
      "login": {},
      "partnerId": 1,
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allClientsAccess` | boolean | Whether the authenticated user can access all client companies. |
| `companies` | array<object> | Companies accessible by the authenticated user. |
| `login` | object | Login details for the authenticated Doyle HCM user, including email when available. |
| `partnerId` | number | Partner identifier for the authenticated Doyle HCM / Worklio user context. |
| `role` | string | Authenticated Worklio role for the Doyle HCM user context. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/me` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

