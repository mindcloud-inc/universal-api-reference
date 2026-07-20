# UiPath Orchestrator: Start jobs



```
POST https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/start-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/start-jobs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "startInfo.releaseKey": "string",
  "startInfo.strategy": "All"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/start-jobs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "startInfo.releaseKey": "string",
    "startInfo.strategy": "All"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startInfo.releaseKey` | string | yes | The process release key to start. |
| `startInfo.strategy` | string | yes | Job start strategy, such as All or Specific. Default: `All`. |
| `startInfo.robotIds[]` | array<number> | no | Robot IDs for Specific strategy. |
| `startInfo.noOfRobots` | number | no | Number of robots to start for robot-count strategies. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BatchExecutionKey": "string",
      "CreationTime": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "Key": "string",
      "Source": "string",
      "State": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BatchExecutionKey` | string |  |
| `CreationTime` | date |  |
| `Id` | number |  |
| `Key` | string |  |
| `Source` | string |  |
| `State` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `POST /odata/Jobs/UiPath.Server.Configuration.OData.StartJobs` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-jobs.md) for the provider-specific parameters and requirements.

