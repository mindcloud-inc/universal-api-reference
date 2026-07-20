# CheckFlow: Remove Tag Assignment



```
DELETE https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/remove-tag-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/remove-tag-assignment?connectionId=$CONNECTION_ID&tagKey=835bf84f-2068-4c20-9c27-4bfac6efccfc&assignmentKey=47ee26a3-92ab-40e0-97d3-23d78796c0aa&assignmentType=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagKey": "835bf84f-2068-4c20-9c27-4bfac6efccfc",
  "assignmentKey": "47ee26a3-92ab-40e0-97d3-23d78796c0aa",
  "assignmentType": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/remove-tag-assignment?${params}`, {
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
| `tagKey` | string | yes | The key of the tag assignment to remove. Example: `835bf84f-2068-4c20-9c27-4bfac6efccfc`. |
| `assignmentKey` | string | yes | The key of the checklist or task the tag is being removed from. Example: `47ee26a3-92ab-40e0-97d3-23d78796c0aa`. |
| `assignmentType` | number | yes | 1 for checklist, 3 for task. Example: `1`. |
| `parentKey` | string | no | Required when removing a tag from a task. The checklist key that contains the task. Example: `47ee26a3-92ab-40e0-97d3-23d78796c0aa`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CheckFlow API returns.

## Native endpoint

Through the native CheckFlow API, this operation is `DELETE /api/tag/assignment` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-assignment.md) for the provider-specific parameters and requirements.

