# Receipt Bot Universal API Examples

These examples use the MindCloud API key and Receipt Bot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Statement Details

Retrieves statement details from Receipt Bot by document ID.

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

Example response:

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

See the full [Get Statement Details action reference](actions/get-statement-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/receiptBot/latest/actions/get-statement-details).

## Upload File

Uploads a base64-encoded file to Receipt Bot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/receiptBot/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/receiptBot/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Upload File action reference](actions/upload-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/receiptBot/latest/actions/upload-file).
