# validTo: Get Bulk Validation Progress

Retrieves bulk validation progress from validTo.

```
GET https://connect.mindcloud.co/v1/universal/validTo/latest/actions/get-bulk-validation-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a validTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/get-bulk-validation-progress?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validTo/latest/actions/get-bulk-validation-progress?${params}`, {
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
| `jobId` | string | yes | The bulk validation job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {},
      "created_at": "string",
      "job_id": "string",
      "message": "string",
      "pending": 1,
      "results": {},
      "status": "string",
      "success": true,
      "total": 1,
      "verified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object | Analysis summary for the uploaded list. |
| `created_at` | string | The date and time the list was created. |
| `job_id` | string | The job_id corresponding to the list status being checked. |
| `message` | string | Describes API result. |
| `pending` | number | The number of emails still pending verification. |
| `results` | object | Verification result totals for the list. |
| `status` | string | The status of the list. |
| `success` | boolean | Whether the API request call was successful. |
| `total` | number | The total number of emails in the list. |
| `verified` | number | The number of emails already verified. |

## Native endpoint

Through the native validTo API, this operation is `GET /bulk/:jobId` (base URL `https://api.validto.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-validation-progress.md) for the provider-specific parameters and requirements.

