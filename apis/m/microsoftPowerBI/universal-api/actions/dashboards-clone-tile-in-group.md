# Microsoft Power BI: Clone Tile In Group



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/dashboards-clone-tile-in-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/dashboards-clone-tile-in-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "dashboardId": "string",
  "tileId": "string",
  "targetDashboardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/dashboards-clone-tile-in-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "dashboardId": "string",
    "tileId": "string",
    "targetDashboardId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace ID |
| `dashboardId` | string | yes | The dashboard ID |
| `tileId` | string | yes | The tile ID |
| `targetDashboardId` | string | yes | The target dashboard ID |
| `positionConflictAction` | object | no | Optional. A parameter for specifying an action in case of a position conflict. If there's a conflict and this parameter isn't provided, then the default value Tail will be applied. If there's no conflict, then the cloned tile will have the same position as in the source. |
| `targetModelId` | string | no | Optional. A parameter for specifying a target model ID. When cloning a tile linked to a dataset, pass the target model ID to rebind the new tile to a different dataset. |
| `targetReportId` | string | no | Optional. A parameter for specifying a target report ID. When cloning a tile linked to a report, pass the target report ID to rebind the new tile to a different report. |
| `targetWorkspaceId` | string | no | Optional. A parameter for specifying a target workspace ID. An empty GUID (00000000-0000-0000-0000-000000000000) indicates **My workspace**. If this parameter isn't provided, the tile will be cloned within the same workspace as the source tile. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/dashboards/[:dashboardId]/tiles/[:tileId]/Clone` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dashboards-clone-tile-in-group.md) for the provider-specific parameters and requirements.

