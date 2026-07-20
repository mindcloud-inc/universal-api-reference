# Escrow.com: Get Current Customer

Retrieves current customer details from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-current-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-current-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-current-customer?${params}`, {
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
      "accountType": "string",
      "company": {},
      "customerEmailVerification": {},
      "electronicVerification": {},
      "email": "ava@example.com",
      "id": 1,
      "verification": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string | Escrow.com account type. |
| `company` | object | Company details for the account. |
| `customerEmailVerification` | object | Email verification details. |
| `electronicVerification` | object | Electronic verification details and supported document configuration. |
| `email` | string | Customer email address. |
| `id` | number | Escrow.com customer ID. |
| `verification` | object | Verification status details. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /customer/me` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-customer.md) for the provider-specific parameters and requirements.

