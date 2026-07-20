# DocuPanda - Document Understanding: Retrieve review by standardization ID

Retrieves a review by standardization ID from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-standardization-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-standardization-review?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-standardization-review?${params}`, {
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
| `review_id` | string | no |  |
| `standardization_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "documentId": "string",
      "schemaId": "string",
      "standardizationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | An exact copy of the original standardization JSON object, except every value is replaced with a dictionary with the following values: - **value**: The original value - **review**:    - **page**: The page number on which the value was found    - **confidence**: The confidence score of the value extraction    - **boundingBox**: The bounding box of the value on the page. These will be normalized coordinates 0..1 for the page size, in the format x1y1x2y2:       - **x1**: The x-coordinate of the top left start of the bounding box       - **y1**: The y-coordinate of the top left start of the bounding box       - **x2**: The width of the bottom right of the bounding box       - **y2**: The height of the bottom right of the bounding box |
| `documentId` | string | Unique identifier of the document. |
| `schemaId` | string | Unique identifier of the schema used for standardization. |
| `standardizationId` | string | Unique identifier of the standardization object. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /review` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-standardization-review.md) for the provider-specific parameters and requirements.

