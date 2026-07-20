# Meisterplan: Delete Milestone

Deletes an existing milestone from Meisterplan.

```
DELETE https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-milestone?connectionId=$CONNECTION_ID&scenarioId=string&projectId=string&milestoneId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scenarioId": "string",
  "projectId": "string",
  "milestoneId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-milestone?${params}`, {
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
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `projectId` | string | yes | Internal Meisterplan project identifier. |
| `milestoneId` | string | yes | Internal Meisterplan milestone identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Meisterplan API returns.

## Native endpoint

Through the native Meisterplan API, this operation is `DELETE /scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-milestone.md) for the provider-specific parameters and requirements.

