# ServiceM8: Create Job



```
POST https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyUuid` | string | no | Existing client UUID to attach to the new job. |
| `status` | string | no | Initial ServiceM8 job status. |
| `jobAddress` | string | no | Address for the new job. |
| `jobDescription` | string | no | Description for the new job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordUuid` | string | UUID of the created job. |

## Native endpoint

Through the native ServiceM8 API, this operation is `POST /api_1.0/job.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

