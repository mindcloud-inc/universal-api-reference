# Procore: Create Action Plan

Creates a new action plan in Procore.

```
POST https://connect.mindcloud.co/v1/universal/procore/latest/actions/create-action-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Procore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/procore/latest/actions/create-action-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "plan": {},
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/procore/latest/actions/create-action-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "plan": {},
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `plan` | object | yes | Action plan payload object. |
| `projectId` | string | yes | Unique identifier for the project. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Procore API returns.

## Native endpoint

Through the native Procore API, this operation is `POST /rest/v1.0/projects/:project_id/action_plans/plans` (base URL `https://api.procore.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action-plan.md) for the provider-specific parameters and requirements.

