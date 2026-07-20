# PlagiarismCheck.org: Submit Plagiarism Check



```
POST https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-plagiarism-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-plagiarism-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-plagiarism-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Plain text content to check for plagiarism. The official docs require at least 80 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiReportId": {},
      "createdAt": "string",
      "customAuthor": {},
      "deletedAt": {},
      "filename": "Ava Chen",
      "groupId": {},
      "id": 1,
      "isDeleted": true,
      "language": "string",
      "pages": 1,
      "reportId": {},
      "state": 1,
      "submittedAt": "string",
      "updatedAt": "string",
      "userId": 1,
      "version": {},
      "words": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiReportId` | object |  |
| `createdAt` | string |  |
| `customAuthor` | object |  |
| `deletedAt` | object |  |
| `filename` | string |  |
| `groupId` | object |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `language` | string |  |
| `pages` | number |  |
| `reportId` | object |  |
| `state` | number |  |
| `submittedAt` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |
| `version` | object |  |
| `words` | number |  |

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `POST /api/v1/text` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-plagiarism-check.md) for the provider-specific parameters and requirements.

