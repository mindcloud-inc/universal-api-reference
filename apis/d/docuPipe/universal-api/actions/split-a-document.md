# DocuPipe: Split a Document

Splits a document in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/split-a-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/split-a-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/split-a-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Unique identifier of the document to be split. |
| `instructions` | string | no | Instructions for how the splitting should be done (optional). |
| `dataset` | string | no | Dataset to assign to the newly generated documents. |
| `filenamePrefix` | string | no | Prefix to use for the filenames of the newly generated documents. |
| `displayMode` | list | no | *Advanced Feature* Mode of display to run. The options are: `auto`: AI decides how to display the document (default) `spatial`: Display text spatially, as it appears in the document `sections`: Display text from top to bottom as sections, with tables appearing as markdown `image`: Display as an image. One of: `auto`, `image`, `sections`, `spatial`. |

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

Through the native DocuPipe API, this operation is `POST /document/split` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-a-document.md) for the provider-specific parameters and requirements.

