# CircleCI: List Insight Workflow Jobs



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-insight-workflow-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-insight-workflow-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-insight-workflow-jobs?${params}`, {
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
      "durationMetrics": {},
      "name": "Ava Chen",
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
| `durationMetrics` | object |  |
| `name` | string |  |
| `status` | string |  |
| `successRate` | number |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /insights/:project_slug/workflows/:workflow_name/jobs` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-insight-workflow-jobs.md) for the provider-specific parameters and requirements.

