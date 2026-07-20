# Smartcat: Get Document

Retrieves document details from the Smartcat account.

```
GET https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=abc_9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "abc_9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | Document ID in the format documentId_targetLanguageId Example: `abc_9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deadline": "2026-05-07T12:00:00.000Z",
      "documentDisassemblingStatus": "string",
      "externalId": "string",
      "filename": "Ava Chen",
      "fullPath": "string",
      "id": "string",
      "name": "Ava Chen",
      "placeholdersAreEnabled": true,
      "pretranslateCompleted": true,
      "projectId": "string",
      "readyForCompletion": true,
      "revisionLabel": "string",
      "sourceLanguage": "string",
      "status": "string",
      "targetLanguage": "string",
      "wordsCount": 1,
      "workflowStages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date | Document creation timestamp |
| `deadline` | date | Document deadline |
| `documentDisassemblingStatus` | string | Document disassembling status |
| `externalId` | string | External document identifier |
| `filename` | string | Stored filename |
| `fullPath` | string | Document full path |
| `id` | string | Document ID |
| `name` | string | Document display name |
| `placeholdersAreEnabled` | boolean | Whether placeholders are enabled |
| `pretranslateCompleted` | boolean | Whether pretranslation has completed |
| `projectId` | string | Parent project ID |
| `readyForCompletion` | boolean | Whether the document is ready for completion |
| `revisionLabel` | string | Smartcat revision label |
| `sourceLanguage` | string | Source language code |
| `status` | string | Document status |
| `targetLanguage` | string | Target language code |
| `wordsCount` | number | Document word count |
| `workflowStages` | array<object> | Workflow stages for the document |

## Native endpoint

Through the native Smartcat API, this operation is `GET /api/integration/v1/document` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

