# Rillion Prime: Add Invoice Receipt To Invoice Queue



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/add-invoice-receipt-to-invoice-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/add-invoice-receipt-to-invoice-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "updateInvoiceReceiptRequest": {},
  "updateInvoiceReceiptRequestInvoiceNo": 1,
  "updateInvoiceReceiptRequestInvoiceSeries": "string",
  "updateInvoiceReceiptRequestArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
  "updateInvoiceReceiptRequestErrorText": "string",
  "updateInvoiceReceiptRequestQueueStatus": 1,
  "updateInvoiceReceiptRequestStatus": 1,
  "updateInvoiceReceiptRequestVoucherNo": 1,
  "updateInvoiceReceiptRequestVoucherSeries": "string",
  "updateInvoiceReceiptRequestInvoiceExternalId": "string",
  "updateInvoiceReceiptRequestInvoiceExternalSource": "string",
  "role": "Administrator"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/add-invoice-receipt-to-invoice-queue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "updateInvoiceReceiptRequest": {},
    "updateInvoiceReceiptRequestInvoiceNo": 1,
    "updateInvoiceReceiptRequestInvoiceSeries": "string",
    "updateInvoiceReceiptRequestArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "updateInvoiceReceiptRequestErrorText": "string",
    "updateInvoiceReceiptRequestQueueStatus": 1,
    "updateInvoiceReceiptRequestStatus": 1,
    "updateInvoiceReceiptRequestVoucherNo": 1,
    "updateInvoiceReceiptRequestVoucherSeries": "string",
    "updateInvoiceReceiptRequestInvoiceExternalId": "string",
    "updateInvoiceReceiptRequestInvoiceExternalSource": "string",
    "role": "Administrator",
    "updateInvoiceReceiptRequest": {},
    "updateInvoiceReceiptRequestInvoiceNo": 1,
    "updateInvoiceReceiptRequestInvoiceSeries": "string",
    "updateInvoiceReceiptRequestArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "updateInvoiceReceiptRequestErrorText": "string",
    "updateInvoiceReceiptRequestQueueStatus": 1,
    "updateInvoiceReceiptRequestStatus": 1,
    "updateInvoiceReceiptRequestVoucherNo": 1,
    "updateInvoiceReceiptRequestVoucherSeries": "string",
    "updateInvoiceReceiptRequestInvoiceExternalId": "string",
    "updateInvoiceReceiptRequestInvoiceExternalSource": "string",
    "role": "Administrator",
    "updateInvoiceReceiptRequest": {},
    "updateInvoiceReceiptRequestInvoiceNo": 1,
    "updateInvoiceReceiptRequestInvoiceSeries": "string",
    "updateInvoiceReceiptRequestArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "updateInvoiceReceiptRequestErrorText": "string",
    "updateInvoiceReceiptRequestQueueStatus": 1,
    "updateInvoiceReceiptRequestStatus": 1,
    "updateInvoiceReceiptRequestVoucherNo": 1,
    "updateInvoiceReceiptRequestVoucherSeries": "string",
    "updateInvoiceReceiptRequestInvoiceExternalId": "string",
    "updateInvoiceReceiptRequestInvoiceExternalSource": "string",
    "role": "Administrator"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateInvoiceReceiptRequest` | object | yes | Request body value for UpdateInvoiceReceiptRequest. |
| `updateInvoiceReceiptRequestInvoiceNo` | number | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceNo. |
| `updateInvoiceReceiptRequestInvoiceSeries` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceSeries. |
| `updateInvoiceReceiptRequestArrivalAccountCodingDate` | date | yes | Request body value for UpdateInvoiceReceiptRequest ArrivalAccountCodingDate. |
| `updateInvoiceReceiptRequestErrorText` | string | yes | Request body value for UpdateInvoiceReceiptRequest ErrorText. |
| `updateInvoiceReceiptRequestQueueStatus` | number | yes | Request body value for UpdateInvoiceReceiptRequest QueueStatus. |
| `updateInvoiceReceiptRequestStatus` | number | yes | Request body value for UpdateInvoiceReceiptRequest Status. |
| `updateInvoiceReceiptRequestVoucherNo` | number | yes | Request body value for UpdateInvoiceReceiptRequest VoucherNo. |
| `updateInvoiceReceiptRequestVoucherSeries` | string | yes | Request body value for UpdateInvoiceReceiptRequest VoucherSeries. |
| `updateInvoiceReceiptRequestInvoiceExternalId` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceExternalId. |
| `updateInvoiceReceiptRequestInvoiceExternalSource` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceExternalSource. |
| `role` | string | yes | Request body value for Role. Example: `Administrator`. |
| `updateInvoiceReceiptRequest` | object | yes | Request body value for UpdateInvoiceReceiptRequest. |
| `updateInvoiceReceiptRequestInvoiceNo` | number | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceNo. |
| `updateInvoiceReceiptRequestInvoiceSeries` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceSeries. |
| `updateInvoiceReceiptRequestArrivalAccountCodingDate` | date | yes | Request body value for UpdateInvoiceReceiptRequest ArrivalAccountCodingDate. |
| `updateInvoiceReceiptRequestErrorText` | string | yes | Request body value for UpdateInvoiceReceiptRequest ErrorText. |
| `updateInvoiceReceiptRequestQueueStatus` | number | yes | Request body value for UpdateInvoiceReceiptRequest QueueStatus. |
| `updateInvoiceReceiptRequestStatus` | number | yes | Request body value for UpdateInvoiceReceiptRequest Status. |
| `updateInvoiceReceiptRequestVoucherNo` | number | yes | Request body value for UpdateInvoiceReceiptRequest VoucherNo. |
| `updateInvoiceReceiptRequestVoucherSeries` | string | yes | Request body value for UpdateInvoiceReceiptRequest VoucherSeries. |
| `updateInvoiceReceiptRequestInvoiceExternalId` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceExternalId. |
| `updateInvoiceReceiptRequestInvoiceExternalSource` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceExternalSource. |
| `role` | string | yes | Request body value for Role. Example: `Administrator`. |
| `updateInvoiceReceiptRequest` | object | yes | Request body value for UpdateInvoiceReceiptRequest. |
| `updateInvoiceReceiptRequestInvoiceNo` | number | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceNo. |
| `updateInvoiceReceiptRequestInvoiceSeries` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceSeries. |
| `updateInvoiceReceiptRequestArrivalAccountCodingDate` | date | yes | Request body value for UpdateInvoiceReceiptRequest ArrivalAccountCodingDate. |
| `updateInvoiceReceiptRequestErrorText` | string | yes | Request body value for UpdateInvoiceReceiptRequest ErrorText. |
| `updateInvoiceReceiptRequestQueueStatus` | number | yes | Request body value for UpdateInvoiceReceiptRequest QueueStatus. |
| `updateInvoiceReceiptRequestStatus` | number | yes | Request body value for UpdateInvoiceReceiptRequest Status. |
| `updateInvoiceReceiptRequestVoucherNo` | number | yes | Request body value for UpdateInvoiceReceiptRequest VoucherNo. |
| `updateInvoiceReceiptRequestVoucherSeries` | string | yes | Request body value for UpdateInvoiceReceiptRequest VoucherSeries. |
| `updateInvoiceReceiptRequestInvoiceExternalId` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceExternalId. |
| `updateInvoiceReceiptRequestInvoiceExternalSource` | string | yes | Request body value for UpdateInvoiceReceiptRequest InvoiceExternalSource. |
| `role` | string | yes | Request body value for Role. Example: `Administrator`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `PUT /invoicequeue/receipt` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-invoice-receipt-to-invoice-queue.md) for the provider-specific parameters and requirements.

