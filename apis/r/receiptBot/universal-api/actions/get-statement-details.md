# Receipt Bot: Get Statement Details

Retrieves statement details from Receipt Bot by document ID.

```
GET https://connect.mindcloud.co/v1/universal/receiptBot/latest/actions/get-statement-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Receipt Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/receiptBot/latest/actions/get-statement-details?connectionId=$CONNECTION_ID&documentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/receiptBot/latest/actions/get-statement-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | number | yes | Receipt Bot document identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bizDocSeq": 1,
      "businessId": "string",
      "businessName": "Ava Chen",
      "eventId": "string",
      "eventType": "string",
      "file": {
        "documentId": 1,
        "documentTypeId": 1,
        "documentTypeName": "Ava Chen",
        "fileName": "Ava Chen",
        "source": "string",
        "uploadDate": 1,
        "uploadUserEmail": "ava@example.com"
      },
      "occurredAt": 1,
      "statement": {
        "bizDocSeq": 1,
        "chargeablePages": 1,
        "closingBalance": 1,
        "dateFrom": 1,
        "dateTo": 1,
        "documentSubType": "string",
        "openingBalance": 1,
        "paymentMethod": {},
        "processingNotes": [
          {}
        ],
        "processStatus": "string",
        "title": "string",
        "transactions": [
          {}
        ],
        "transactionsCount": 1
      },
      "trigger": "string",
      "webhookStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bizDocSeq` | number | Receipt Bot business document sequence. |
| `businessId` | string | Receipt Bot business identifier. |
| `businessName` | string | Receipt Bot business name. |
| `eventId` | string | Receipt Bot event identifier. |
| `eventType` | string | Receipt Bot event type. |
| `file.documentId` | number | Document identifier. |
| `file.documentTypeId` | number | Document type identifier. |
| `file.documentTypeName` | string | Document type label. |
| `file.fileName` | string | Uploaded file name. |
| `file.source` | string | Upload source. |
| `file.uploadDate` | number | Unix timestamp when the file was uploaded. |
| `file.uploadUserEmail` | string | Email of the upload user. |
| `occurredAt` | number | Unix timestamp for the event. |
| `statement.bizDocSeq` | number | Statement business document sequence. |
| `statement.chargeablePages` | number | Chargeable page count. |
| `statement.closingBalance` | number | Closing balance when available. |
| `statement.dateFrom` | number | Start date as unix timestamp when available. |
| `statement.dateTo` | number | End date as unix timestamp when available. |
| `statement.documentSubType` | string | Statement subtype when available. |
| `statement.openingBalance` | number | Opening balance when available. |
| `statement.paymentMethod` | object | Payment method details when available. |
| `statement.processingNotes` | array<object> | Provider processing notes. |
| `statement.processStatus` | string | Processing status. |
| `statement.title` | string | Statement title when available. |
| `statement.transactions` | array<object> | Extracted transactions. |
| `statement.transactionsCount` | number | Count of extracted transactions. |
| `trigger` | string | Provider trigger label. |
| `webhookStatus` | string | Webhook delivery status when applicable. |

## Native endpoint

Through the native Receipt Bot API, this operation is `POST /StatementDetails` (base URL `https://api.receipt-bot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statement-details.md) for the provider-specific parameters and requirements.

