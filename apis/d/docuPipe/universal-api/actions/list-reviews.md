# DocuPipe: List Reviews

Retrieves reviews from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-reviews?${params}`, {
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
| `includeData` | boolean | no | Whether to include the data payload in the response Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "dataset": "string",
      "displayMode": "string",
      "documentId": "string",
      "fieldMetadata": {},
      "filename": "Ava Chen",
      "jobId": "string",
      "metadata": {},
      "pageMap": {},
      "reviewId": "string",
      "reviewState": "string",
      "schemaId": "string",
      "schemaName": "Ava Chen",
      "standardizationId": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | An exact copy of the original standardization JSON object, except every value is replaced with a dictionary with the following values: - **value**: The original value - **review**:    - **page**: The page number on which the value was found    - **confidence**: The confidence score of the value extraction    - **boundingBox**: The bounding box of the value on the page. These will be normalized coordinates 0..1 for the page size, in the format x1y1x2y2:       - **x1**: The x-coordinate of the top left start of the bounding box       - **y1**: The y-coordinate of the top left start of the bounding box       - **x2**: The width of the bottom right of the bounding box       - **y2**: The height of the bottom right of the bounding box |
| `dataset` | string | Name of the dataset to which the document belongs |
| `displayMode` | string | Display mode actually used during standardization. |
| `documentId` | string | Unique identifier of the document. |
| `fieldMetadata` | object | Per-field extraction metadata mapping dot-paths to page numbers and confidence levels. |
| `filename` | string | Name of the file that was standardized. |
| `jobId` | string | Unique identifier of the job that created the standardization. |
| `metadata` | object | Metadata associated with the document that originated this standardization. This just echoes any metadata you have previously posted on document creation. |
| `pageMap` | object | Maps dot-paths to 1-indexed page numbers where each value was extracted from. |
| `reviewId` | string | Unique identifier of the review object. |
| `reviewState` | string | State of the review. Can be 'unverified', 'verified' or 'rejected'. Unverified means the review is AI-generated and has not been reviewed by a human. Verified means the review has been reviewed by a human and approved. Rejected means the review has been reviewed by a human and marked as incorrect. |
| `schemaId` | string | Unique identifier of the schema used for standardization. |
| `schemaName` | string | Name of the schema used for standardization. |
| `standardizationId` | string | Unique identifier of the standardization object. |
| `timestamp` | string | Timestamp of the standardization job. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /reviews` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

