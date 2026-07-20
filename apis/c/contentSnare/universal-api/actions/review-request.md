# Content Snare: Review Request

Reviews a request field in Content Snare.

```
PUT https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/review-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/review-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/review-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Request ID. |
| `answersAttributes[]` | array<object> | no | <b>DEPRECATED</b> |
| `answersAttributes[].id` | string | no | Answer id |
| `answersAttributes[].rejectionComment` | string | no | A message for your client letting them know why you rejected the answer and what they need to do to fix it |
| `answersAttributes[].status` | string | no | Answer status. <br>Set status 'approved' for the following actions: approve. <br> status 'todo' for the following actions: remove reject, remove approval. <br>Set status 'redo' for the following actions: reject. |
| `rejectionComment` | string | no | A message for your client letting them know why you rejected the field and what they need to do to fix it |
| `status` | string | no | Field status. <br>Set status 'approved' for the following actions: approve. <br>Set status 'done' for the following actions: submit for review, remove reject, remove approval. <br>Set status 'todo' for the following actions: revise. <br>Set status 'redo' for the following actions: reject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {
          "id": "string",
          "rejection_comment": "string",
          "status": "string"
        }
      ],
      "id": "string",
      "rejection_comment": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers[].id` | string |  |
| `answers[].rejection_comment` | string |  |
| `answers[].status` | string |  |
| `id` | string |  |
| `rejection_comment` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `PUT /partner_api/v1/fields/{id}/review` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/review-request.md) for the provider-specific parameters and requirements.

