# UiPath Orchestrator: Stop job



```
PUT https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/stop-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/stop-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": 1,
  "strategy": "Stop"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/stop-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": 1,
    "strategy": "Stop"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | number | yes | The numeric job ID to stop. |
| `strategy` | string | yes | The stop strategy, such as Kill or Stop. Default: `Stop`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "State": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `State` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `POST /odata/Jobs/UiPath.Server.Configuration.OData.StopJob` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-job.md) for the provider-specific parameters and requirements.

