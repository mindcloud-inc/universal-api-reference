# Lob: Verify Bank Account



```
PUT https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-bank-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bankId": "string",
  "amounts[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-bank-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bankId": "string",
    "amounts[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bankId` | string | yes | Bank account ID. |
| `amounts[]` | array<number> | yes | Two micro-deposit amounts in cents. |

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

Through the native Lob API, this operation is `POST /bank_accounts/:bank_id/verify` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-bank-account.md) for the provider-specific parameters and requirements.

