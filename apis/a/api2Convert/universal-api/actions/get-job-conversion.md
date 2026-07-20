# Api2Convert: Get Job Conversion

Retrieves a job conversion from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-conversion?connectionId=$CONNECTION_ID&jobId=string&conversionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "conversionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-job-conversion?${params}`, {
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
| `jobId` | string | yes | ID of the job. |
| `conversionId` | string | yes | ID of the conversion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "id": "string",
      "metadata": {},
      "options": {},
      "output_target": [
        {}
      ],
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Conversion category. |
| `id` | string | Identifier of the job conversion. |
| `metadata` | object | Conversion metadata. |
| `options` | object | Selected conversion options. |
| `output_target` | array<object> | Configured output targets. |
| `target` | string | Target conversion format. |

## Native endpoint

Through the native Api2Convert API, this operation is `GET /jobs/:job_id/conversions/:conversion_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-conversion.md) for the provider-specific parameters and requirements.

