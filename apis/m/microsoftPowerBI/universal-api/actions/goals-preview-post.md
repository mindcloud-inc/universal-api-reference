# Microsoft Power BI: Post



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goals-preview-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goals-preview-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "scorecardId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goals-preview-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "scorecardId": "string",
    "name": "Ava Chen"
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
| `name` | string | yes | The goal name |
| `completionDate` | date | no | Optional. The UTC timestamp for the completion date of the goal. The time portion of the timestamp is zero. |
| `datesFormatString` | string | no | Optional. The custom format string for dates. |
| `parentId` | string | no | Optional. The ID of the parent goal, if defined. |
| `startDate` | date | no | Optional. The UTC timestamp for the start date of the goal. The time portion of the timestamp is zero. |
| `valuesFormatString` | string | no | Optional. The custom format string for values. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/scorecards([:scorecardId])/goals` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/goals-preview-post.md) for the provider-specific parameters and requirements.

