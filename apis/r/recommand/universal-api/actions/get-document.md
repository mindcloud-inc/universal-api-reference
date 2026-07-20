# Recommand: Get Document

Retrieves a document record from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-document?connectionId=$CONNECTION_ID&documentid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-document?${params}`, {
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
| `documentid` | string | yes | documentId parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": {
        "companyId": "string",
        "countryC1": "string",
        "createdAt": "string",
        "direction": "string",
        "docTypeId": "string",
        "emailRecipients": [
          "ava@example.com"
        ],
        "envelopeId": "string",
        "id": "string",
        "labels": [
          {}
        ],
        "parsed": {},
        "peppolConversationId": "string",
        "peppolMessageId": "string",
        "processId": "string",
        "readAt": "string",
        "receivedPeppolSignalMessage": "string",
        "receiverId": "string",
        "senderId": "string",
        "sentOverEmail": true,
        "sentOverPeppol": true,
        "teamId": "string",
        "type": "string",
        "updatedAt": "string",
        "validation": {},
        "xml": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document` | object |  |
| `document.companyId` | string |  |
| `document.countryC1` | string |  |
| `document.createdAt` | string |  |
| `document.direction` | string |  |
| `document.docTypeId` | string |  |
| `document.emailRecipients` | array<string> |  |
| `document.envelopeId` | string |  |
| `document.id` | string |  |
| `document.labels` | array<object> |  |
| `document.parsed` | object |  |
| `document.peppolConversationId` | string |  |
| `document.peppolMessageId` | string |  |
| `document.processId` | string |  |
| `document.readAt` | string |  |
| `document.receivedPeppolSignalMessage` | string |  |
| `document.receiverId` | string |  |
| `document.senderId` | string |  |
| `document.sentOverEmail` | boolean |  |
| `document.sentOverPeppol` | boolean |  |
| `document.teamId` | string |  |
| `document.type` | string |  |
| `document.updatedAt` | string |  |
| `document.validation` | object |  |
| `document.xml` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/documents/:documentId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

