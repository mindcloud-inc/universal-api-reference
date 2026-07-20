# Deep Infra: Get Current Account



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-current-account?${params}`, {
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
      "company": "string",
      "country": "string",
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "email_verified": true,
      "first_name": "Ava",
      "is_business_account": true,
      "is_team_account": true,
      "last_name": "Chen",
      "name": "Ava Chen",
      "provider": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Business account company name. |
| `country` | string | Account country. |
| `display_name` | string | Configured display name. |
| `email` | string | Account email address. |
| `email_verified` | boolean | Whether the email address is verified. |
| `first_name` | string | Account holder first name. |
| `is_business_account` | boolean | Whether the account is a business account. |
| `is_team_account` | boolean | Whether this account belongs to a team. |
| `last_name` | string | Account holder last name. |
| `name` | string | Account holder name. |
| `provider` | string | Identity provider name. |
| `uid` | string | Deep Infra account user identifier. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/me` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account.md) for the provider-specific parameters and requirements.

