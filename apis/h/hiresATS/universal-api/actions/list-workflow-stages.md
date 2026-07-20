# 100Hires ATS: List Workflow Stages

Lists the workflow stages in 100Hires ATS.

```
GET https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-workflow-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-workflow-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-workflow-stages?${params}`, {
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
| `workflowId` | number | no | Optional workflow ID to restrict stages to a specific workflow. |
| `jobId` | number | no | Optional job ID to load the workflow stages used by a specific job. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | no | Optional target company ID. Defaults to the authenticated company. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `GET /workflows/stages` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-stages.md) for the provider-specific parameters and requirements.

