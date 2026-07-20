# Airparser Universal API Examples

These examples use the MindCloud API key and Airparser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inboxes

Retrieves all inbox records from Airparser.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/list-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airparser/latest/actions/list-inboxes?${params}`, {
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
      "cooldown": {
        "alertEmailH": 1,
        "alertEmailLastTs": {},
        "alertIgfailedH": 1,
        "alertIgfailedLastTs": {},
        "alertInboxDeleted": {}
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailPrefix": "ava@example.com",
      "emailProcessing": "ava@example.com",
      "fieldsMeta": {
        "attachmentsNb": true,
        "bcc": true,
        "cc": true,
        "content": true,
        "contentPlaintext": true,
        "contentPlaintextMd": true,
        "contentType": true,
        "credits": true,
        "docId": true,
        "docUrl": true,
        "downloadUrl": true,
        "filename": true,
        "from": true,
        "fromName": true,
        "name": "Ava Chen",
        "originalRecipient": true,
        "pages": true,
        "parentData": true,
        "parentId": true,
        "receivedAtDate": true,
        "receivedAtDatetime": true,
        "receivedAtTime": true,
        "replyTo": true,
        "subject": true,
        "to": true
      },
      "format": {
        "dateIn": "string",
        "dateOut": "string",
        "datetimeIn": "string",
        "datetimeOut": "string",
        "numberSepIn": "string",
        "numberSepOut": "string",
        "timeIn": "string",
        "timeOut": "string"
      },
      "gptEngine": "string",
      "gptModel": "string",
      "ignoreImg": true,
      "ignoreUrls": true,
      "isActive": true,
      "name": "Ava Chen",
      "ocrEngine": "string",
      "ownerId": "string",
      "pp": {
        "code": "string",
        "isEnabled": true
      },
      "retention": 1,
      "schema": {
        "updatedAt": {}
      },
      "splitPdfEvery": 1,
      "stats": {
        "docsFailed": 1,
        "docsParsed": 1,
        "docsTotal": 1,
        "lastActivity": {}
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "useXmlParser": true
    }
  ],
  "meta": {}
}
```

See the full [List Inboxes action reference](actions/list-inboxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airparser/latest/actions/list-inboxes).

## Clone Extraction Schema

Clones an extraction schema between Airparser inboxes.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/clone-extraction-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string",
  "destinationInboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airparser/latest/actions/clone-extraction-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string",
    "destinationInboxId": "string"
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

See the full [Clone Extraction Schema action reference](actions/clone-extraction-schema.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airparser/latest/actions/clone-extraction-schema).
