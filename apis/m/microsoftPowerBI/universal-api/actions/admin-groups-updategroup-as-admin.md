# Microsoft Power BI: Groups UpdateGroupAsAdmin



```
PUT https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-updategroup-as-admin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-updategroup-as-admin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-updategroup-as-admin', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace ID |
| `id` | string | yes | The workspace ID |
| `capacityId` | string | no | The capacity ID |
| `dashboards[]` | array<object> | no | The dashboards that belong to the group |
| `dataflowStorageId` | string | no | The Power BI dataflow storage account ID |
| `dataflows[]` | array<object> | no | The dataflows that belong to the group |
| `datasets[]` | array<object> | no | The datasets that belong to the group |
| `defaultDatasetStorageFormat` | object | no | The default dataset storage format in the workspace. Returned only when isOnDedicatedCapacity is true |
| `description` | string | no | The group description |
| `hasWorkspaceLevelSettings` | boolean | no | Whether the workspace has custom settings |
| `isOnDedicatedCapacity` | boolean | no | Whether the group is assigned to a dedicated capacity |
| `isReadOnly` | boolean | no | Whether the group is read-only |
| `logAnalyticsWorkspace` | object | no | The Log Analytics workspace assigned to the group. This is returned only when retrieving a single group. |
| `name` | string | no | The group name |
| `pipelineId` | string | no | The deployment pipeline ID that the workspace is assigned to. |
| `reports[]` | array<object> | no | The reports that belong to the group |
| `state` | string | no | The group state |
| `type` | object | no | The type of group being returned. |
| `users[]` | array<object> | no | (Empty value) The users that belong to the group and their access rights. This property will be removed from the payload response in an upcoming release. You can retrieve user information on a Power BI item (such as a report or a dashboard) by using the Get Group Users As Admin API call, or the PostWorkspaceInfo API call with the getArtifactUsers parameter. |
| `workbooks[]` | array<object> | no | The workbooks that belong to the group |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `PATCH admin/groups/[:groupId]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-groups-updategroup-as-admin.md) for the provider-specific parameters and requirements.

