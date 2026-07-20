# Groups UpdateGroupAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `admin/groups/[:groupId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups UpdateGroupAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-update-group-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `id` | body | `string` | yes | The workspace ID |
| `capacityId` | body | `string` | no | The capacity ID |
| `dashboards[]` | body | `array<object>` | no | The dashboards that belong to the group |
| `dataflowStorageId` | body | `string` | no | The Power BI dataflow storage account ID |
| `dataflows[]` | body | `array<object>` | no | The dataflows that belong to the group |
| `datasets[]` | body | `array<object>` | no | The datasets that belong to the group |
| `defaultDatasetStorageFormat` | body | `object` | no | The default dataset storage format in the workspace. Returned only when isOnDedicatedCapacity is true |
| `description` | body | `string` | no | The group description |
| `hasWorkspaceLevelSettings` | body | `boolean` | no | Whether the workspace has custom settings |
| `isOnDedicatedCapacity` | body | `boolean` | no | Whether the group is assigned to a dedicated capacity |
| `isReadOnly` | body | `boolean` | no | Whether the group is read-only |
| `logAnalyticsWorkspace` | body | `object` | no | The Log Analytics workspace assigned to the group. This is returned only when retrieving a single group. |
| `name` | body | `string` | no | The group name |
| `pipelineId` | body | `string` | no | The deployment pipeline ID that the workspace is assigned to. |
| `reports[]` | body | `array<object>` | no | The reports that belong to the group |
| `state` | body | `string` | no | The group state |
| `type` | body | `object` | no | The type of group being returned. |
| `users[]` | body | `array<object>` | no | (Empty value) The users that belong to the group and their access rights. This property will be removed from the payload response in an upcoming release. You can retrieve user information on a Power BI item (such as a report or a dashboard) by using the Get Group Users As Admin API call, or the PostWorkspaceInfo API call with the getArtifactUsers parameter. |
| `workbooks[]` | body | `array<object>` | no | The workbooks that belong to the group |
