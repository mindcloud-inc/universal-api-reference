# Rillion Prime: Unknown Invoice For Role



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/unknown-invoice-for-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/unknown-invoice-for-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "unknownRole": "string",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/unknown-invoice-for-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "unknownRole": "string",
    "note": "string",
    "unknownRole": "string",
    "note": "string",
    "unknownRole": "string",
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | Path value for InvoiceId. |
| `unknownRole` | string | yes | Request body value for UnknownRole. |
| `note` | string | yes | Request body value for Note. |
| `unknownRole` | string | yes | Request body value for UnknownRole. |
| `note` | string | yes | Request body value for Note. |
| `unknownRole` | string | yes | Request body value for UnknownRole. |
| `note` | string | yes | Request body value for Note. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoice/unknown/:invoiceId` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unknown-invoice-for-role.md) for the provider-specific parameters and requirements.

