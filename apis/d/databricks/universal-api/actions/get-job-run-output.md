# Databricks: Get Job Run Output

Retrieves output for a Databricks job run.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-job-run-output
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-job-run-output?connectionId=$CONNECTION_ID&runId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-job-run-output?${params}`, {
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
| `runId` | number | yes | The canonical identifier for the run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert_output": {},
      "clean_rooms_notebook_output": {},
      "dashboard_output": {},
      "dbt_output": {},
      "error": "string",
      "error_trace": "string",
      "info": "string",
      "logs": "string",
      "logs_truncated": true,
      "metadata": {},
      "notebook_output": {},
      "run_job_output": {},
      "sql_output": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_output` | object |  |
| `clean_rooms_notebook_output` | object |  |
| `dashboard_output` | object |  |
| `dbt_output` | object |  |
| `error` | string |  |
| `error_trace` | string |  |
| `info` | string |  |
| `logs` | string |  |
| `logs_truncated` | boolean |  |
| `metadata` | object |  |
| `notebook_output` | object |  |
| `run_job_output` | object |  |
| `sql_output` | object |  |

## Native endpoint

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.2/jobs/runs/get-output` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-run-output.md) for the provider-specific parameters and requirements.

