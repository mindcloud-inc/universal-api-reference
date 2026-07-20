# Sempico Solutions SMS: Get Account Information



```
GET https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/get-account-information?${params}`, {
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
      "balance_daily_block": true,
      "balance_limit": 1,
      "balance_units": 1,
      "block": true,
      "can_send_bulk": true,
      "can_send_restapi": true,
      "company_name": "Ava Chen",
      "confirmed": 1,
      "currency": "string",
      "e_mail": "string",
      "finance": {},
      "id_subparent": 1,
      "login": "string",
      "name": "Ava Chen",
      "phone": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance_daily_block` | boolean | Whether the account is daily-balance blocked. |
| `balance_limit` | number | Configured balance limit. |
| `balance_units` | number | Available account balance units. |
| `block` | boolean | Whether the account is blocked. |
| `can_send_bulk` | boolean | Whether bulk SMS sending is enabled. |
| `can_send_restapi` | boolean | Whether REST API sending is enabled. |
| `company_name` | string | Company name. |
| `confirmed` | number | Account confirmation flag. |
| `currency` | string | Account currency. |
| `e_mail` | string | Primary account email. |
| `finance` | object | Finance and credit status. |
| `id_subparent` | number | Parent account ID. |
| `login` | string | Account login. |
| `name` | string | Account holder name. |
| `phone` | number | Account phone number. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `GET /me` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

