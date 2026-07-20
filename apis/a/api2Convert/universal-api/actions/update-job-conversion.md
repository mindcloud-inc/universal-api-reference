# Api2Convert: Update Job Conversion

Updates an existing job conversion in Api2Convert.

```
PUT https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "conversionId": "string",
  "conversionPatch": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/update-job-conversion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "conversionId": "string",
    "conversionPatch": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | Unique identifier of the job that owns the conversion. |
| `conversionId` | string | yes | Unique identifier of the conversion to update. |
| `conversionPatch` | object | yes | Patch payload for the conversion, including options and metadata. |

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

Through the native Api2Convert API, this operation is `PATCH /jobs/:job_id/conversions/:conversion_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job-conversion.md) for the provider-specific parameters and requirements.

