# Microsoft Power BI: Patch By ID



```
PUT https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goals-preview-patch-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goals-preview-patch-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "scorecardId": "string",
  "goalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goals-preview-patch-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "scorecardId": "string",
    "goalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The unique identifier of the workspace |
| `scorecardId` | string | yes | The unique identifier of the scorecard |
| `goalId` | string | yes | The unique identifier of the goal |
| `aggregations[]` | array<object> | no | The list of aggregated properties of the goal |
| `completionDate` | date | no | The UTC timestamp for the completion date of the goal. The time portion of the timestamp is zero. |
| `createdTime` | date | no | The UTC time at creation |
| `datesFormatString` | string | no | datesFormatString |
| `description` | string | no | The goal description |
| `goalValues[]` | array<object> | no | The list of goal value check-ins |
| `hasStatusRules` | boolean | no | Whether the goal has status rules defined |
| `id` | string | no | The goal ID |
| `lastModifiedTime` | date | no | The UTC time at last modification |
| `level` | number | no | The nested level of the goal in the parent-child hierarchy of scorecard goals |
| `name` | string | no | The goal name |
| `notesCount` | number | no | notesCount |
| `parentId` | string | no | The ID of the parent goal, if defined. |
| `permissions` | object | no | The goal permissions |
| `rank` | number | no | The rank of the goal within the ordered set of sibling goals |
| `startDate` | date | no | The UTC timestamp for the start date of the goal. The time portion of the timestamp is zero. |
| `statusRules` | object | no | The goal status rules |
| `valuesFormatString` | string | no | valuesFormatString |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `PATCH groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/goals-preview-patch-by-id.md) for the provider-specific parameters and requirements.

