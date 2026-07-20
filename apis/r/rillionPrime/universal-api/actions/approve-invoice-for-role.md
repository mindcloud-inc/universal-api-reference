# Rillion Prime: Approve Invoice For Role



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-invoice-for-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-invoice-for-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "signingRole": "string",
  "invoiceAccountCoding": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-invoice-for-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "signingRole": "string",
    "invoiceAccountCoding": ["string"],
    "signingRole": "string",
    "invoiceAccountCoding": ["string"],
    "signingRole": "string",
    "invoiceAccountCoding": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | Path value for InvoiceId. |
| `quickSign` | boolean | no | Set to true to use quick-sign behavior when supported. |
| `signingRole` | string | yes | Request body value for SigningRole. |
| `invoiceAccountCoding` | array | yes | Request body value for InvoiceAccountCoding. |
| `signingRole` | string | yes | Request body value for SigningRole. |
| `invoiceAccountCoding` | array | yes | Request body value for InvoiceAccountCoding. |
| `signingRole` | string | yes | Request body value for SigningRole. |
| `invoiceAccountCoding` | array | yes | Request body value for InvoiceAccountCoding. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoice/approve/:invoiceId` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-invoice-for-role.md) for the provider-specific parameters and requirements.

