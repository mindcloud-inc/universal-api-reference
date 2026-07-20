# CircleCI: Get Job Timeseries



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-job-timeseries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-job-timeseries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-job-timeseries?${params}`, {
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
| `projectSlug` | string | no | Project slug in the form vcs/org/repo. |
| `workflow_name` | string | no | Workflow name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "runTime": 1,
      "status": "string",
      "successRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `runTime` | number |  |
| `status` | string |  |
| `successRate` | number |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /insights/time-series/:project_slug/workflows/:workflow_name/jobs` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-timeseries.md) for the provider-specific parameters and requirements.

