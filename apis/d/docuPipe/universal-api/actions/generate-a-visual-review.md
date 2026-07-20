# DocuPipe: Generate a Visual Review

Creates a visual review in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/generate-a-visual-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/generate-a-visual-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "standardizationIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/generate-a-visual-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "standardizationIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `standardizationIds[]` | array<string> | yes | Unique identifier of the standardization object. |
| `reviewInstructions` | string | no | Instructions for the review process. You may optionally specify which fields you want to localize, and give the AI tips to improve review performance |
| `highGranularity` | boolean | no | When enabled, the review will locate individual sub-fields within compound items (e.g. each field within a line item). This provides more precise bounding boxes but costs 4 credits/page instead of 2. Default: `false`. |

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

Through the native DocuPipe API, this operation is `POST /review/batch` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-a-visual-review.md) for the provider-specific parameters and requirements.

