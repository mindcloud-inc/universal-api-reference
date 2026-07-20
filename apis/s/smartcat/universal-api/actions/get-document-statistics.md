# Smartcat: Get Document Statistics

Retrieves document statistics from the Smartcat account.

```
GET https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-document-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-document-statistics?connectionId=$CONNECTION_ID&documentId=abc_9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "abc_9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-document-statistics?${params}`, {
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
| `onlyExactMatches` | boolean | no | Whether to count only exact translation memory matches Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "changeStamp": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "documentId": "string",
      "externalTag": "string",
      "isConfirmedByPretranslate": true,
      "jobId": "string",
      "language": "string",
      "projectId": "string",
      "stageType": "string",
      "userId": "string",
      "vendorAccountId": "string",
      "wordcounts": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | The account in which the project was created |
| `changeStamp` | string | Change stamp |
| `date` | date | The date for which statistics were collected |
| `documentId` | string | Document ID |
| `externalTag` | string | External system tag |
| `isConfirmedByPretranslate` | boolean | Whether the statistics reflect pretranslated confirmations |
| `jobId` | string | Job ID when applicable |
| `language` | string | Target language |
| `projectId` | string | Project ID |
| `stageType` | string | Workflow stage type |
| `userId` | string | User ID |
| `vendorAccountId` | string | Vendor account ID when applicable |
| `wordcounts` | object | Word count model for segment confirmation statistics |

## Native endpoint

Through the native Smartcat API, this operation is `GET /api/integration/v1/document/statistics` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-statistics.md) for the provider-specific parameters and requirements.

