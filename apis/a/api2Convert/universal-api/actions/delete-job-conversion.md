# Api2Convert: Delete Job Conversion

Deletes a job conversion from Api2Convert.

```
DELETE https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job-conversion?connectionId=$CONNECTION_ID&jobId=string&conversionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "conversionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-job-conversion?${params}`, {
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
| `jobId` | string | yes | Unique identifier of the job that owns the conversion. |
| `conversionId` | string | yes | Unique identifier of the conversion to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversion_id": "string",
      "deleted": true,
      "job_id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversion_id` | string | Identifier of the deleted conversion. |
| `deleted` | boolean | Whether the conversion was deleted. |
| `job_id` | string | Identifier of the parent job. |
| `message` | string | Deletion result message. |

## Native endpoint

Through the native Api2Convert API, this operation is `DELETE /jobs/:job_id/conversions/:conversion_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job-conversion.md) for the provider-specific parameters and requirements.

