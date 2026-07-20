# Airparser: List Inboxes

Retrieves all inbox records from Airparser.

```
GET https://connect.mindcloud.co/v1/universal/airparser/latest/actions/list-inboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airparser `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cooldown.alertEmailH` | number |  |
| `cooldown.alertEmailLastTs` | object |  |
| `cooldown.alertIgfailedH` | number |  |
| `cooldown.alertIgfailedLastTs` | object |  |
| `cooldown.alertInboxDeleted` | object |  |
| `createdAt` | date |  |
| `emailPrefix` | string |  |
| `emailProcessing` | string |  |
| `fieldsMeta.attachmentsNb` | boolean |  |
| `fieldsMeta.bcc` | boolean |  |
| `fieldsMeta.cc` | boolean |  |
| `fieldsMeta.content` | boolean |  |
| `fieldsMeta.contentPlaintext` | boolean |  |
| `fieldsMeta.contentPlaintextMd` | boolean |  |
| `fieldsMeta.contentType` | boolean |  |
| `fieldsMeta.credits` | boolean |  |
| `fieldsMeta.docId` | boolean |  |
| `fieldsMeta.docUrl` | boolean |  |
| `fieldsMeta.downloadUrl` | boolean |  |
| `fieldsMeta.filename` | boolean |  |
| `fieldsMeta.from` | boolean |  |
| `fieldsMeta.fromName` | boolean |  |
| `fieldsMeta.name` | string |  |
| `fieldsMeta.originalRecipient` | boolean |  |
| `fieldsMeta.pages` | boolean |  |
| `fieldsMeta.parentData` | boolean |  |
| `fieldsMeta.parentId` | boolean |  |
| `fieldsMeta.receivedAtDate` | boolean |  |
| `fieldsMeta.receivedAtDatetime` | boolean |  |
| `fieldsMeta.receivedAtTime` | boolean |  |
| `fieldsMeta.replyTo` | boolean |  |
| `fieldsMeta.subject` | boolean |  |
| `fieldsMeta.to` | boolean |  |
| `format.dateIn` | string |  |
| `format.dateOut` | string |  |
| `format.datetimeIn` | string |  |
| `format.datetimeOut` | string |  |
| `format.numberSepIn` | string |  |
| `format.numberSepOut` | string |  |
| `format.timeIn` | string |  |
| `format.timeOut` | string |  |
| `gptEngine` | string |  |
| `gptModel` | string |  |
| `ignoreImg` | boolean |  |
| `ignoreUrls` | boolean |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `ocrEngine` | string |  |
| `ownerId` | string |  |
| `pp.code` | string |  |
| `pp.isEnabled` | boolean |  |
| `retention` | number |  |
| `schema.updatedAt` | object |  |
| `splitPdfEvery` | number |  |
| `stats.docsFailed` | number |  |
| `stats.docsParsed` | number |  |
| `stats.docsTotal` | number |  |
| `stats.lastActivity` | object |  |
| `updatedAt` | date |  |
| `useXmlParser` | boolean |  |

## Native endpoint

Through the native Airparser API, this operation is `GET /inboxes` (base URL `https://api.airparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inboxes.md) for the provider-specific parameters and requirements.

