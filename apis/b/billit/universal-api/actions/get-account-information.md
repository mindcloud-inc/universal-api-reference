# Billit: Get Account Information

Retrieves account information for the authenticated Billit user.

```
GET https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-account-information?${params}`, {
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
      "Companies": [
        {}
      ],
      "Email": "ava@example.com",
      "LoginOrRegisterNeeded": true,
      "UserCompanyRoles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Companies` | array<object> | Companies available to the authenticated Billit user. |
| `Email` | string | Billit account email address. |
| `LoginOrRegisterNeeded` | boolean | Whether Billit requires login or registration for the current account. |
| `UserCompanyRoles` | array<object> | Billit company role assignments for the authenticated user. |

## Native endpoint

Through the native Billit API, this operation is `GET /v1/account/accountInformation` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

