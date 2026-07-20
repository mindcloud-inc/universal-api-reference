# Jotform: Get Submission

Retrieves a submission from Jotform.

```
GET https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-submission?connectionId=$CONNECTION_ID&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-submission?${params}`, {
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
| `submissionId` | string | yes | Submission ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "created_at": "string",
      "form_id": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> |  |
| `created_at` | string |  |
| `form_id` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `GET /submission/:submissionId` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission.md) for the provider-specific parameters and requirements.

