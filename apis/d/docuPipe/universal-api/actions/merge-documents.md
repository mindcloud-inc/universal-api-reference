# DocuPipe: Merge Documents

Merges documents in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/merge-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/merge-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds[]": [
    "string"
  ],
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/merge-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds[]": ["string"],
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds[]` | array<string> | yes | List of unique identifiers of the documents to be merged. The order of IDs determines the order of documents in the merged output. Must contain at least two document IDs. |
| `filename` | string | yes | Filename of the newly generated document after merging. |
| `dataset` | string | no | Dataset to assign to the newly generated document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "success": true,
      "timestamp": "2026-05-07T12:00:00.000Z"
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
| `timestamp` | date | Timestamp of when the job was submitted. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /documents/merge` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-documents.md) for the provider-specific parameters and requirements.

