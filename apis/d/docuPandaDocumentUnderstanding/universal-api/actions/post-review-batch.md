# DocuPanda - Document Understanding: Generate a Visual Review

Creates a visual review in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-review-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-review-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "standardizationIds": "string",
  "standardizationIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-review-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "standardizationIds": "string",
    "standardizationIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `standardizationIds` | list<string> | yes | Unique identifier of the standardization object. |
| `standardizationIds[]` | array<string> | yes | Unique identifier of the standardization object. |
| `reviewInstructions` | string | no |  |
| `highGranularity` | boolean | no | When enabled, the review will locate individual sub-fields within compound items (e.g. each field within a line item). This provides more precise bounding boxes but costs 4 credits/page instead of 2. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobIds": [
        "string"
      ],
      "reviewIds": [
        "string"
      ],
      "standardizationIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobIds` | array<string> | Unique identifiers of the jobs. |
| `reviewIds` | array<string> | Unique identifiers of the review objects which will be generated. |
| `standardizationIds` | array<string> | Unique identifiers of the standardization objects under review. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /review/batch` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-review-batch.md) for the provider-specific parameters and requirements.

