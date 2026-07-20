# CheckFlow: Assign Tag To Checklist Or Task



```
POST https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/assign-tag-to-checklist-or-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/assign-tag-to-checklist-or-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagKey": "835bf84f-2068-4c20-9c27-4bfac6efccfc",
  "assignmentKey": "27217bc9-1f00-460e-bf41-3821cd37beaf",
  "assignmentType": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/assign-tag-to-checklist-or-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagKey": "835bf84f-2068-4c20-9c27-4bfac6efccfc",
    "assignmentKey": "27217bc9-1f00-460e-bf41-3821cd37beaf",
    "assignmentType": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagKey` | string | yes | The key of the tag to assign. Example: `835bf84f-2068-4c20-9c27-4bfac6efccfc`. |
| `assignmentKey` | string | yes | The key of the checklist or task the tag is being assigned to. Example: `27217bc9-1f00-460e-bf41-3821cd37beaf`. |
| `assignmentType` | number | yes | 1 for checklist, 3 for task. Example: `1`. |
| `parentKey` | string | no | Required when assigning a tag to a task. The checklist key that contains the task. Example: `27217bc9-1f00-460e-bf41-3821cd37beaf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignmentKey": "string",
      "assignmentType": 1,
      "isNew": true,
      "parentKey": "string",
      "tagKey": "string",
      "tagName": "Ava Chen",
      "teamID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignmentKey` | string | The checklist or task key that received the tag. |
| `assignmentType` | number | 1 for checklist assignments, 3 for task assignments. |
| `isNew` | boolean | Whether the returned assignment record was newly created. |
| `parentKey` | string | The checklist key when the assignment targets a task; null for checklist assignments. |
| `tagKey` | string | The key of the assigned tag. |
| `tagName` | string | The display name of the assigned tag. |
| `teamID` | number | The numeric team ID that owns the assignment. |

## Native endpoint

Through the native CheckFlow API, this operation is `POST /api/tag/assignment` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-tag-to-checklist-or-task.md) for the provider-specific parameters and requirements.

