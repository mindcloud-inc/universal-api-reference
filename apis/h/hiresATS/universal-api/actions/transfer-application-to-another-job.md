# 100Hires ATS: Transfer Application To Another Job

Transfers an application to another job in 100Hires ATS.

```
PUT https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/transfer-application-to-another-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/transfer-application-to-another-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "4804833",
  "jobId": "275694"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/transfer-application-to-another-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "4804833",
    "jobId": "275694"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Application ID to transfer. Example: `4804833`. |
| `jobId` | number | yes | Destination job ID. Example: `275694`. |
| `stageId` | number | no | Optional destination stage ID. Example: `251850`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated related application resources to include. Example: `candidate,job`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `POST /applications/:id/transfer` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-application-to-another-job.md) for the provider-specific parameters and requirements.

