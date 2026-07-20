# Docparser: Get Document Status

Retrieves status details for a Docparser document.

```
GET https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-document-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-document-status?connectionId=$CONNECTION_ID&parserId=tiumtyrcddpn&documentId=52d17ca7ac28434b11c5037127144251" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "tiumtyrcddpn",
  "documentId": "52d17ca7ac28434b11c5037127144251"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-document-status?${params}`, {
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
| `parserId` | string | yes | Use the parser ID returned by List Document Parsers. Example: `tiumtyrcddpn`. |
| `documentId` | string | yes | Use the document ID returned by a parsed-data action. Example: `52d17ca7ac28434b11c5037127144251`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dispatchedWebhook": true,
      "dispatchedWebhookAt": 1,
      "dispatchedWebhookProblem": true,
      "filename": "Ava Chen",
      "fileSource": "string",
      "firstProcessedAt": 1,
      "importedAt": 1,
      "importingInProgress": true,
      "mimeType": "string",
      "ocrStartedAt": 1,
      "pages": 1,
      "preprocessedAt": 1,
      "preprocessingInProgressAt": 1,
      "processedAt": 1,
      "processingInProgress": true,
      "remoteId": "string",
      "supported": true,
      "token": "string",
      "uploadedAt": 1,
      "webhookDispatchingInProgress": true,
      "webhooksCreated": 1,
      "webhooksSent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dispatchedWebhook` | boolean |  |
| `dispatchedWebhookAt` | number |  |
| `dispatchedWebhookProblem` | boolean |  |
| `filename` | string |  |
| `fileSource` | string |  |
| `firstProcessedAt` | number |  |
| `importedAt` | number |  |
| `importingInProgress` | boolean |  |
| `mimeType` | string |  |
| `ocrStartedAt` | number |  |
| `pages` | number |  |
| `preprocessedAt` | number |  |
| `preprocessingInProgressAt` | number |  |
| `processedAt` | number |  |
| `processingInProgress` | boolean |  |
| `remoteId` | string |  |
| `supported` | boolean |  |
| `token` | string |  |
| `uploadedAt` | number |  |
| `webhookDispatchingInProgress` | boolean |  |
| `webhooksCreated` | number |  |
| `webhooksSent` | number |  |

## Native endpoint

Through the native Docparser API, this operation is `GET /v2/document/status/:PARSER_ID/:DOCUMENT_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-status.md) for the provider-specific parameters and requirements.

