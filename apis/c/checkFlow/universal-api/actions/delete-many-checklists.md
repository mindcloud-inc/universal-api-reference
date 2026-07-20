# CheckFlow: Delete Many Checklists



```
DELETE https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-many-checklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-many-checklists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-many-checklists?${params}`, {
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
| `checklistIds[]` | array<number> | no | A list of specific checklist IDs to delete. Example: `1001,1002`. |
| `templateKeys[]` | array<string> | no | Template keys whose matching checklists should be deleted. Example: `0e7ad584-7788-4ab1-95a6-ca0a5b444cbb`. |
| `checklistStatus` | string | no | Status filter used when deleting by template keys. Example: `ALL`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CheckFlow API returns.

## Native endpoint

Through the native CheckFlow API, this operation is `DELETE /api/checklist/delete-many` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-many-checklists.md) for the provider-specific parameters and requirements.

