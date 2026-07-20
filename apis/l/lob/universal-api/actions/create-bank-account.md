# Lob: Create Bank Account



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-bank-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "routingNumber": "string",
  "accountNumber": "string",
  "signatory": "string",
  "accountType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-bank-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "routingNumber": "string",
    "accountNumber": "string",
    "signatory": "string",
    "accountType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description for the bank account. |
| `routingNumber` | string | yes | Valid US routing number. |
| `accountNumber` | string | yes | Bank account number. |
| `signatory` | string | yes | Signatory printed on checks. |
| `accountType` | string | yes | Type of entity that holds the account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_number": "string",
      "account_type": "string",
      "bank_name": "Ava Chen",
      "date_created": "string",
      "date_modified": "string",
      "description": "string",
      "id": "string",
      "metadata": {},
      "object": "string",
      "routing_number": "string",
      "signatory": "string",
      "signature_url": "https://example.com",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_number` | string |  |
| `account_type` | string |  |
| `bank_name` | string |  |
| `date_created` | string |  |
| `date_modified` | string |  |
| `description` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `routing_number` | string |  |
| `signatory` | string |  |
| `signature_url` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Lob API, this operation is `POST /bank_accounts` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bank-account.md) for the provider-specific parameters and requirements.

