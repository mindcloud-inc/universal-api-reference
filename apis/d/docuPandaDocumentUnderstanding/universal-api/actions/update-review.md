# DocuPanda - Document Understanding: Update a Review

Updates an existing review in DocuPanda.

```
PUT https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "review_id": "string",
  "reviewStatus": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "review_id": "string",
    "reviewStatus": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | The data to update the review with. This should be a dictionary with the same structure as the review object. If omitted, the data will not be updated. |
| `review_id` | string | yes |  |
| `reviewStatus` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reviewId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reviewId` | string | Unique identifier of the review object. |
| `success` | boolean | Whether the review update was successful. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /review/:review_id/update` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-review.md) for the provider-specific parameters and requirements.

