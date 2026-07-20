# TelTel: Get Account Balance

Retrieves account balance details from your TelTel account.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-account-balance?${params}`, {
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
      "balance": 1,
      "credit": 1,
      "creditLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Current account balance. |
| `credit` | number | Current account credit. |
| `creditLimit` | number | Account credit limit. |

## Native endpoint

Through the native TelTel API, this operation is `GET /account/balance` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-balance.md) for the provider-specific parameters and requirements.

