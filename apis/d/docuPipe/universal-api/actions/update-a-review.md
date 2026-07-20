# DocuPipe: Update a Review

Updates a review in DocuPipe.

```
PUT https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/update-a-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/update-a-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reviewId": "string",
  "reviewStatus": "rejected"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/update-a-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reviewId": "string",
    "reviewStatus": "rejected"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reviewId` | string | yes |  |
| `data` | object | no | The data to update the review with. This should be a dictionary with the same structure as the review object. If omitted, the data will not be updated. |
| `reviewStatus` | list | yes | Use this field to indicate whether the posted object is verified to be correct, incorrect, or not yet fully verified. One of: `rejected`, `unverified`, `verified`. |

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

Through the native DocuPipe API, this operation is `POST /review/:reviewId/update` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-review.md) for the provider-specific parameters and requirements.

