# Ringg AI: Edit Knowledge Base

Updates an existing knowledge base in Ringg AI.

```
PUT https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/edit-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/edit-knowledge-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "kbId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/edit-knowledge-base', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "kbId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `kbId` | string | yes | (Required) ID of the knowledge base to edit |
| `filesToRemove` | string | no | (Optional) JSON string array of file IDs to remove |
| `urlsToRemove` | string | no | (Optional) JSON string array of URLs to remove |
| `faqsToRemove` | string | no | (Optional) JSON string array of FAQ IDs to remove |
| `newFiles[]` | array<string> | no | (Optional) Array of new files to upload |
| `newUrls` | string | no | (Optional) JSON string array of new URLs to add |
| `newFaqs` | string | no | (Optional) JSON string array of new FAQ objects |
| `newFilesMetadata` | string | no | (Optional) JSON string object with metadata for new files |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemsRemoved": 1,
      "kbId": "string",
      "message": "string",
      "newFiles": [
        {
          "fileId": "string",
          "filename": "Ava Chen",
          "processingStatus": "string"
        }
      ],
      "newFilesQueued": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemsRemoved` | number |  |
| `kbId` | string |  |
| `message` | string |  |
| `newFiles` | array<object> |  |
| `newFiles[].fileId` | string |  |
| `newFiles[].filename` | string |  |
| `newFiles[].processingStatus` | string |  |
| `newFilesQueued` | number |  |

## Native endpoint

Through the native Ringg AI API, this operation is `PATCH /external/kb` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-knowledge-base.md) for the provider-specific parameters and requirements.

