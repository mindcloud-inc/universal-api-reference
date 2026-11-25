# Celigo: List Jobs



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-jobs?${params}`, {
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
| `integrationId` | list<string> | no | Only return jobs for this integration. Send it with Flow ID when the flow belongs to an integration. |
| `flowId` | list<string> | no | Only return jobs for this flow. Pick from List Flows. |
| `status` | list<string> | no | Only return jobs in this status. One of: `canceled`, `canceling`, `completed`, `failed`, `queued`, `retrying`, `running`. |
| `type` | list<string> | no | Job type. Flow, Retry and Bulk Retry are parent (run-level) jobs; Export, Import and Tool are step jobs and need Flow Job ID, Export ID or Import ID. One of: `bulk_retry`, `export`, `flow`, `import`, `retry`, `tool`. |
| `createdAtGte` | date | no | Only return jobs created at or after this time (ISO 8601). |
| `createdAtLte` | date | no | Only return jobs created at or before this time. To page, pass the last job's createdAt minus 1 ms. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flowJobId` | string | no | Parent flow-run job ID. Required for Export, Import and Tool step jobs. |
| `exportId` | string | no | Only return jobs for this export step. |
| `importId` | string | no | Only return jobs for this import step. |
| `numErrorGte` | number | no | Only return jobs with at least this many errors. |
| `numErrorLte` | number | no | Only return jobs with at most this many errors. |
| `numSuccessGte` | number | no | Only return jobs with at least this many successful records. |
| `numSuccessLte` | number | no | Only return jobs with at most this many successful records. |
| `numIgnoreGte` | number | no | Only return jobs with at least this many ignored records. |
| `numIgnoreLte` | number | no | Only return jobs with at most this many ignored records. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Celigo API returns.

## Native endpoint

Through the native Celigo API, this operation is `GET /jobs` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

