# Microsoft Power BI: WorkspaceInfo PostWorkspaceInfo



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-postworkspaceinfo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-postworkspaceinfo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-postworkspaceinfo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetExpressions` | boolean | no | Whether to return dataset expressions (DAX and Mashup queries). If you set this parameter to true, you must fully enable metadata scanning in order for data to be returned. For more information, see Enable tenant settings for metadata scanning. |
| `datasetSchema` | boolean | no | Whether to return dataset schema (tables, columns and measures). If you set this parameter to true, you must fully enable metadata scanning in order for data to be returned. For more information, see Enable tenant settings for metadata scanning. |
| `datasourceDetails` | boolean | no | Whether to return data source details |
| `getArtifactUsers` | boolean | no | Whether to return user details for a Power BI item (such as a report or a dashboard) |
| `lineage` | boolean | no | Whether to return lineage info (upstream dataflows, tiles, data source IDs) |
| `workspaces[]` | array<string> | no | The required workspace IDs to be scanned (supports 1 to 100 workspace IDs) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST admin/workspaces/getInfo` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-workspaceinfo-postworkspaceinfo.md) for the provider-specific parameters and requirements.

