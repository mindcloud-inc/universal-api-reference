# Rillion Prime: Change Invoice Queue Account Coding Date



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/change-invoice-queue-account-coding-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/change-invoice-queue-account-coding-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "changes": {},
  "changesNewAccountCodingDate": "2026-05-07T12:00:00.000Z",
  "changesInvoiceQueueIds": [
    "string"
  ],
  "changesRole": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/change-invoice-queue-account-coding-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "changes": {},
    "changesNewAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "changesInvoiceQueueIds": ["string"],
    "changesRole": "string",
    "changes": {},
    "changesNewAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "changesInvoiceQueueIds": ["string"],
    "changesRole": "string",
    "changes": {},
    "changesNewAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "changesInvoiceQueueIds": ["string"],
    "changesRole": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `changes` | object | yes | Request body value for Changes. |
| `changesNewAccountCodingDate` | date | yes | Request body value for Changes NewAccountCodingDate. |
| `changesInvoiceQueueIds` | array | yes | Request body value for Changes InvoiceQueueIds. |
| `changesRole` | string | yes | Request body value for Changes Role. |
| `changes` | object | yes | Request body value for Changes. |
| `changesNewAccountCodingDate` | date | yes | Request body value for Changes NewAccountCodingDate. |
| `changesInvoiceQueueIds` | array | yes | Request body value for Changes InvoiceQueueIds. |
| `changesRole` | string | yes | Request body value for Changes Role. |
| `changes` | object | yes | Request body value for Changes. |
| `changesNewAccountCodingDate` | date | yes | Request body value for Changes NewAccountCodingDate. |
| `changesInvoiceQueueIds` | array | yes | Request body value for Changes InvoiceQueueIds. |
| `changesRole` | string | yes | Request body value for Changes Role. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoicequeue/changeaccountcodingdate` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-invoice-queue-account-coding-date.md) for the provider-specific parameters and requirements.

