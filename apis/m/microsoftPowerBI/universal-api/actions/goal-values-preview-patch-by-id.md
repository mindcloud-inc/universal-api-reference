# Microsoft Power BI: Patch By ID



```
PUT https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-patch-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-patch-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "scorecardId": "string",
  "goalId": "string",
  "timestamp": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-patch-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "scorecardId": "string",
    "goalId": "string",
    "timestamp": "2026-05-07T12:00:00.000Z"
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
| `timestamp` | date | yes | The timestamp for the value of the goal |
| `createdTime` | date | no | The UTC time at creation |
| `forecast` | number | no | The goal value trend forecast |
| `lastModifiedTime` | date | no | The UTC time at last modification |
| `notes[]` | array<object> | no | The notes for the goal |
| `status` | number | no | The ID of the goal status |
| `target` | number | no | The goal target value |
| `targetDisplayString` | string | no | The textual representation of the goal target |
| `trend` | number | no | The goal value trend |
| `value` | number | no | The goal current value |
| `valueDisplayString` | string | no | The textual representation of the current goal value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `PATCH groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/goal-values-preview-patch-by-id.md) for the provider-specific parameters and requirements.

