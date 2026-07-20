# TrueLayer: List Merchant Accounts

Retrieves merchant accounts from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/list-merchant-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/list-merchant-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/list-merchant-accounts?${params}`, {
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
      "account_identifiers": [
        {}
      ],
      "available_balance": 1,
      "currency": "string",
      "current_balance": 1,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_identifiers` | array<object> | Account identifiers such as IBAN or sort code/account number. |
| `available_balance` | number | Available balance when returned. |
| `currency` | string | Merchant account currency. |
| `current_balance` | number | Current balance when returned. |
| `id` | string | Merchant account identifier. |
| `name` | string | Merchant account display name. |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v3/merchant-accounts` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-merchant-accounts.md) for the provider-specific parameters and requirements.

