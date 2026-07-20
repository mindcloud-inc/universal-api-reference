# Microsoft Power BI: Move Goals



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-move-goals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-move-goals" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "scorecardId": "string",
  "goalToMove": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-move-goals', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "scorecardId": "string",
    "goalToMove": {}
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
| `goalToMove` | object | yes | The rank validation information for the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |
| `newNext` | object | no | Optional. The rank validation information for the new next-sibling of the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |
| `newParent` | object | no | Optional. The rank validation information for the new parent of the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |
| `newPrevious` | object | no | Optional. The rank validation information for the new previous-sibling of the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/scorecards([:scorecardId])/MoveGoals()` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scorecards-preview-move-goals.md) for the provider-specific parameters and requirements.

