# Microsoft Power BI: Delete By ID



```
DELETE https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-delete-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-delete-by-id?connectionId=$CONNECTION_ID&groupId=string&scorecardId=string&goalId=string&timestamp=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "scorecardId": "string",
  "goalId": "string",
  "timestamp": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/goal-values-preview-delete-by-id?${params}`, {
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
| `groupId` | string | yes | The unique identifier of the workspace |
| `scorecardId` | string | yes | The unique identifier of the scorecard |
| `goalId` | string | yes | The unique identifier of the goal |
| `timestamp` | date | yes | The timestamp for the value of the goal |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `DELETE groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/goal-values-preview-delete-by-id.md) for the provider-specific parameters and requirements.

