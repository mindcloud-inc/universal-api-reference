# MindCloud: List All Runs



```
GET https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-all-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-all-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-all-runs?${params}`, {
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
| `status` | list<string> | no | Only runs with this status. One of: `cancelled`, `cancelling`, `failed`, `finished`, `interrupted`, `limitExceeded`, `running`, `waiting`. |
| `from` | string | no | Only runs that started at or after this time, within the last 7 days: YYYY-MM-DD (midnight UTC) or an ISO 8601 date-time with a zone. Defaults to midnight UTC 7 days ago. Example: `2026-11-20`. |

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
      "errorCount": 1,
      "finishedOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "infoCount": 1,
      "installationId": "string",
      "operations": 1,
      "startedOn": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "summary": "string",
      "triggerAppSlug": "string",
      "version": "string",
      "warningCount": 1,
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
| `activeStepId` | string | The last step the run reached: while it runs, the step it is on now; once it ends, the step it stopped at. |
| `durationMs` | number | How long the run took, in milliseconds. While it runs, how long it has run so far. |
| `endUserId` | string | The embedded end user the run belongs to, if any. |
| `environmentId` | string | The environment the run targeted. |
| `environmentName` | string | That environment's name. |
| `errorCount` | number | How many errors the run logged. |
| `finishedOn` | date | When the run ended. Empty while it runs. |
| `id` | string | Unique id of the run. |
| `infoCount` | number | How many info entries the run logged. |
| `installationId` | string | The embedded installation the run belongs to, if any. |
| `operations` | number | How many tasks the run used. |
| `startedOn` | date | When the run started. |
| `status` | string | Where the run stands or how it ended: waiting, running, finished, failed, cancelled, interrupted, limitExceeded, or cancelling. |
| `summary` | string | A short summary of what the run did. For a failed or interrupted run, why it stopped. Empty while it runs. |
| `triggerAppSlug` | string | The app that triggered the run. |
| `version` | string | The workflow version that ran, or draft. |
| `warningCount` | number | How many warnings the run logged. |
| `workflowId` | string | The workflow this run belongs to. |
| `workflowName` | string | The workflow's current name. |

## Native endpoint

Through the native MindCloud API, this operation is `GET /v2/runs` (base URL `https://connect.mindcloud.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-runs.md) for the provider-specific parameters and requirements.

