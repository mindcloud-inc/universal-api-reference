# DocuPanda - Document Understanding: Merge Documents

Creates a merged document in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-merge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-merge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds": "string",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-merge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds": "string",
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataset` | string | no | Dataset to assign to the newly generated document. |
| `documentIds` | list<string> | yes | List of unique identifiers of the documents to be merged. The order of IDs determines the order of documents in the merged output. Must contain at least two document IDs. |
| `filename` | string | yes | Filename of the newly generated document after merging. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "success": true,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Unique identifier for the submitted job. |
| `success` | boolean | Whether the job was successfully submitted. |
| `timestamp` | string | Timestamp of when the job was submitted. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /documents/merge` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-merge.md) for the provider-specific parameters and requirements.

