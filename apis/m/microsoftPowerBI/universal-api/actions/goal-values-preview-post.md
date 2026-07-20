# Microsoft Power BI: Post



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-post" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-post', {
  method: 'POST',
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
| `timestamp` | date | yes | The UTC timestamp of the goal value check-in. The time portion of the timestamp is zero. |
| `forecast` | number | no | Optional. The value trend forecast of the goal. |
| `status` | number | no | Optional. The goal status ID. |
| `target` | number | no | Optional. The target value of the goal. |
| `trend` | number | no | Optional. The value trend of the goal. |
| `value` | number | no | Optional. The current value of the goal. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/goal-values-preview-post.md) for the provider-specific parameters and requirements.

