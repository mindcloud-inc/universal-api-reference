# Extracta.ai: Delete Classification Files

Deletes classification files from Extracta.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/delete-classification-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/delete-classification-files?connectionId=$CONNECTION_ID&classificationId=string&batchId=string&fileIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classificationId": "string",
  "batchId": "string",
  "fileIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/delete-classification-files?${params}`, {
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
| `classificationId` | string | yes | Unique identifier for the classification. |
| `batchId` | string | yes | Unique identifier for the batch. |
| `fileIds[]` | array<string> | yes | List of file identifiers to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleteAll": true,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleteAll` | boolean |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `DELETE /documentClassification/deleteFiles` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-classification-files.md) for the provider-specific parameters and requirements.

