# Verifalia: List Validation Jobs

Retrieves email validation jobs from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-validation-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-validation-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-validation-jobs?${params}`, {
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
| `createdOn` | string | no | Filter jobs created on one specific date in YYYY-MM-DD format. |
| `createdOnSince` | string | no | Inclusive start date for the job listing period in YYYY-MM-DD format. |
| `createdOnUntil` | string | no | Inclusive end date for the job listing period in YYYY-MM-DD format. |
| `owner` | string | no | Only return jobs submitted by the specified Verifalia user ID. |
| `sort` | string | no | Sort jobs by `createdOn` or `-createdOn`. |
| `status` | string | no | One or more job statuses to include, separated by commas. |
| `statusExclude` | string | no | One or more job statuses to exclude, separated by commas. |

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
| `id` | string | The validation job ID. |
| `name` | string | The optional user-defined job name. |
| `noOfEntries` | number | The total number of email addresses in the job. |
| `owner` | string | The Verifalia user ID that owns the job. |
| `quality` | string | The requested validation quality level. |
| `retention` | string | The retention period configured for the job. |
| `status` | string | The current validation job status. |
| `submittedOn` | string | When the job was submitted for processing. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /email-validations` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-validation-jobs.md) for the provider-specific parameters and requirements.

