# Retently: Get Feedback

Retrieves a feedback response from Retently by ID.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-feedback?connectionId=$CONNECTION_ID&feedbackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedbackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-feedback?${params}`, {
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
| `feedbackId` | string | yes | Feedback Id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "companyName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "feedbackTags": [
        "string"
      ],
      "firstName": "Ava",
      "lastName": "Chen",
      "score": 1,
      "tags": [
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
| `comment` | string |  |
| `companyName` | string |  |
| `createdDate` | date |  |
| `email` | string |  |
| `feedbackTags` | array<string> |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `score` | number |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/feedback/:feedbackId` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedback.md) for the provider-specific parameters and requirements.

