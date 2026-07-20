# SqlBak: Get Account Information

Retrieves account information from SqlBak.

```
GET https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SqlBak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/get-account-information?${params}`, {
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
      "created_at": 1,
      "credit_usd": 1,
      "email": "ava@example.com",
      "entity": "string",
      "is_suspended": true,
      "managed_accounts": [
        {}
      ],
      "manager_accounts": [
        {}
      ],
      "name": "Ava Chen",
      "subscription": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Account company name when present. |
| `created_at` | number | Account creation time in UNIX milliseconds. |
| `credit_usd` | number | Account credit in USD. |
| `email` | string | Primary account email. |
| `entity` | string | Type of returned entity. |
| `is_suspended` | boolean | Whether the account is suspended. |
| `managed_accounts` | array<object> | Accounts that this account can manage. |
| `manager_accounts` | array<object> | Accounts that can manage this account. |
| `name` | string | Account name. |
| `subscription` | object | Current subscription details. |

## Native endpoint

Through the native SqlBak API, this operation is `GET /me` (base URL `https://sqlbak.com/public-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

