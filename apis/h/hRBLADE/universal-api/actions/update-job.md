# HRBLADE: Update Job



```
PUT https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "forFollowUp": "false",
  "jobId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "forFollowUp": "false",
    "jobId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | no | Company identifier for the job. |
| `description` | string | no | Job description text. |
| `forFollowUp` | boolean | yes | Whether this is a follow-up job posting. Default: `false`. |
| `jobId` | number | yes | Job identifier. |
| `name` | string | no | Job title. |
| `questionPayload1` | string | no | Stringified question object, e.g. {"type":"VIDEO","question":"...","time":"00:01:00","sorting":0}. Example: `JSON string for questions[0] (VIDEO/TEXT/CODE payload)`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "error": true,
      "response": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `error` | boolean |  |
| `response.message` | string |  |

## Native endpoint

Through the native HRBLADE API, this operation is `POST /job/update` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

