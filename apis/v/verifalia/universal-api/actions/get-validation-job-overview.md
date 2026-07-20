# Verifalia: Get Validation Job Overview

Retrieves an email validation job overview from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-validation-job-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-validation-job-overview?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-validation-job-overview?${params}`, {
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
| `id` | string | yes | The Verifalia validation job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientIP": "string",
      "completedOn": "string",
      "createdOn": "string",
      "deduplication": "string",
      "estimatedTimeRemaining": "string",
      "id": "string",
      "name": "Ava Chen",
      "noOfEntries": 1,
      "owner": "string",
      "quality": "string",
      "retention": "string",
      "status": "string",
      "submittedOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientIP` | string | The IP address that created the job. |
| `completedOn` | string | When the job completed, if available. |
| `createdOn` | string | When the job was created. |
| `deduplication` | string | The deduplication algorithm used for the job. |
| `estimatedTimeRemaining` | string | Estimated remaining processing time when Verifalia can determine it. |
| `id` | string | The validation job ID. |
| `name` | string | The optional user-defined job name. |
| `noOfEntries` | number | The total number of email addresses in the job. |
| `owner` | string | The Verifalia user ID that owns the job. |
| `quality` | string | The requested validation quality level. |
| `retention` | string | The retention period configured for the job. |
| `status` | string | The current validation job status. |
| `submittedOn` | string | When the job was submitted for processing. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /email-validations/{id}/overview` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-job-overview.md) for the provider-specific parameters and requirements.

