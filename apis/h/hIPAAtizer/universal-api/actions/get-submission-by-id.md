# HIPAAtizer: Get Submission By ID

Retrieves a submission by ID from HIPAAtizer.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/get-submission-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/get-submission-by-id?connectionId=$CONNECTION_ID&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/get-submission-by-id?${params}`, {
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
| `submissionId` | string | yes | Submission identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "data": {},
      "id": "string",
      "ipAddress": "string",
      "workflowId": "string",
      "workflowVersionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `data` | object |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `workflowId` | string |  |
| `workflowVersionId` | string |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `GET /api/v1/api_key/submissions/:submissionId` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-by-id.md) for the provider-specific parameters and requirements.

