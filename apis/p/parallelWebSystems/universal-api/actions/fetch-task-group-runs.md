# Parallel Web Systems: Fetch Task Group Runs



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/fetch-task-group-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/fetch-task-group-runs?connectionId=$CONNECTION_ID&taskgroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskgroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/fetch-task-group-runs?${params}`, {
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
| `taskgroupId` | string | yes | The Parallel task group ID. |
| `lastEventId` | string | no | Return runs after this event ID. |
| `status` | string | no | Filter task group runs by status. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `includeInput` | boolean | no | Include task run input payloads. |
| `includeOutput` | boolean | no | Include task run output payloads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_id": "string",
      "input": {
        "input": "string",
        "processor": "string",
        "source_policy": {
          "exclude_domains": "string",
          "include_domains": "string"
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_id` | string | Event identifier. |
| `input.input` | string | Task run input payload. |
| `input.processor` | string | Task run processor. |
| `input.source_policy.exclude_domains` | string | Excluded domains filter. |
| `input.source_policy.include_domains` | string | Included domains filter. |
| `type` | string | Event type. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1beta/tasks/groups/:taskgroup_id/runs` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-task-group-runs.md) for the provider-specific parameters and requirements.

