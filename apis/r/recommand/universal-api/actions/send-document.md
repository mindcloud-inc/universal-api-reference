# Recommand: Send Document

Sends a document through the Recommand network.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/send-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/send-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyid": "string",
  "document": {},
  "documenttype": "string",
  "recipient": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/send-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyid": "string",
    "document": {},
    "documenttype": "string",
    "recipient": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyid` | string | yes | companyId parameter. |
| `doctypeid` | string | no | The document type identifier. Not required, only used when documentType is "xml". For supported document types, the doctypeId can be detected automatically from your XML document, if that's not the case you can provide it manually. |
| `document` | object | yes | document body field. |
| `documenttype` | string | yes | The type of document. |
| `email` | object | no | email body field. |
| `pdfgeneration` | object | no | pdfGeneration body field. |
| `processid` | string | no | The process identifier. Not required, only used when documentType is "xml". For supported document types, the processId can be detected automatically from your XML document, if that's not the case you can provide it manually. |
| `recipient` | string | yes | The Peppol address of the recipient. If null, the document will be sent via email only (requires `email.to`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "emailRecipients": [
        "ava@example.com"
      ],
      "envelopeId": "string",
      "id": "string",
      "peppolMessageId": "string",
      "sentOverEmail": true,
      "sentOverPeppol": true,
      "success": true,
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `emailRecipients` | array<string> |  |
| `envelopeId` | string |  |
| `id` | string |  |
| `peppolMessageId` | string |  |
| `sentOverEmail` | boolean |  |
| `sentOverPeppol` | boolean |  |
| `success` | boolean |  |
| `teamId` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/:companyId/send` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-document.md) for the provider-specific parameters and requirements.

