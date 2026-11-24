# MindCloud: List Failed Runs



```
GET https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-failed-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-failed-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-failed-runs?${params}`, {
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
| `workflowId` | list<string> | no | Only runs of this workflow. Example: `Wq3kZ8pLx2Nb`. |
| `from` | date | no | Only runs that started at or after this time. Example: `2026-11-01T00:00:00Z`. |
| `before` | date | no | Only runs that started before this time. Leave empty for runs up to now. Example: `2026-11-23T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeStepId": "string",
      "durationMs": 1,
      "endUserId": "string",
      "environmentId": "string",
      "environmentName": "Ava Chen",
      "finishedOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "installationId": "string",
      "operations": 1,
      "startedOn": "2026-05-07T12:00:00.000Z",
      "summary": "string",
      "version": "string",
      "workflowId": "string",
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeStepId` | string | The step the run stopped at. |
| `durationMs` | number | How long the run took, in milliseconds. |
| `endUserId` | string | The embedded end user the run belongs to, if any. |
| `environmentId` | string | The environment the run targeted. |
| `environmentName` | string | That environment's name. |
| `finishedOn` | date | When the run stopped. |
| `id` | string | Unique id of the run. |
| `installationId` | string | The embedded installation the run belongs to, if any. |
| `operations` | number | How many tasks the run used before it stopped. |
| `startedOn` | date | When the run started. |
| `summary` | string | Why the run stopped: the step name and the error it returned. |
| `version` | string | The workflow version that ran, or draft. |
| `workflowId` | string | The workflow this run belongs to. |
| `workflowName` | string | The workflow's current name. |

## Native endpoint

Through the native MindCloud API, this operation is `GET /v2/failed-runs` (base URL `https://connect.mindcloud.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-failed-runs.md) for the provider-specific parameters and requirements.

