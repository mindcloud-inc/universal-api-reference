# CircleCI: Get Insight Workflow Summary



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-insight-workflow-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-insight-workflow-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-insight-workflow-summary?${params}`, {
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
      "successRate": 1,
      "totalRuns": 1
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
| `successRate` | number |  |
| `totalRuns` | number |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /insights/:project_slug/workflows/:workflow_name/summary` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-insight-workflow-summary.md) for the provider-specific parameters and requirements.

