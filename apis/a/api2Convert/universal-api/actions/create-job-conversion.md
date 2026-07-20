# Api2Convert: Create Job Conversion

Creates a conversion for a job in Api2Convert.

```
POST https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "conversion": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "conversion": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | Unique identifier of the job that owns the conversion. |
| `conversion` | object | yes | Conversion payload for the job, including the target and options. |

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

Through the native Api2Convert API, this operation is `POST /jobs/:job_id/conversions` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-conversion.md) for the provider-specific parameters and requirements.

