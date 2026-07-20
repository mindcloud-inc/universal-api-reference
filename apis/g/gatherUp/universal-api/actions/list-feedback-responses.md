# GatherUp: List Feedback Responses

Retrieves a list of feedback responses from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-feedback-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-feedback-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-feedback-responses?${params}`, {
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
| `businessId` | number | no | Business id (or multiple comma-separated ids.) |
| `feedbackId` | number | no | Feedback id (or multiple comma-separated ids.) |
| `from` | string | no | Received from |
| `page` | number | no | Page Default: `1`. |
| `to` | string | no | Received to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": 1,
      "content": "string",
      "count": 1,
      "date": "string",
      "errorCode": 1,
      "errorMessage": "string",
      "feedbackId": 1,
      "page": 1,
      "pages": 1,
      "perPage": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | number |  |
| `content` | string |  |
| `count` | number |  |
| `date` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `feedbackId` | number |  |
| `page` | number |  |
| `pages` | number |  |
| `perPage` | number |  |
| `type` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /feedbacks/responses/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feedback-responses.md) for the provider-specific parameters and requirements.

