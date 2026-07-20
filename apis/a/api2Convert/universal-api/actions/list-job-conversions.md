# Api2Convert: List Job Conversions

Retrieves conversions for a job from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-conversions?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/list-job-conversions?${params}`, {
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

Through the native Api2Convert API, this operation is `GET /jobs/:job_id/conversions` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-conversions.md) for the provider-specific parameters and requirements.

