# Save Dataflow Gen One As Dataflow Gen Two with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/dataflows/[:gen1DataflowId]/saveAsNativeArtifact`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Save Dataflow Gen One As Dataflow Gen Two](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/save-dataflow-gen-one-as-dataflow-gen-two)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace (group) ID of the gen1 dataflow |
| `gen1DataflowId` | path | `string` | yes | The object ID of the Gen1 dataflow to save as a native artifact |
| `description` | body | `string` | no | Optional description for the new artifact. If not provided or empty, the description from the source dataflow will be copied. Maximum length: 4000 characters |
| `displayName` | body | `string` | no | Optional display name for the new artifact. If not provided or empty, the system will generate a name based on the source dataflow name with a suffix like "\_copy1", "\_copy2", etc. to avoid naming conflicts. Maximum length: 200 characters |
| `includeSchedule` | body | `boolean` | no | Whether to include the refresh schedule from the source dataflow in the migration. If true, attempts to copy the existing schedule to the new artifact in disabled state. If false, the new artifact will be created without a schedule. |
| `targetWorkspaceId` | body | `string` | no | Optional target workspace ID where the new artifact will be created. If not provided or empty, the new artifact will be created in the same workspace as the source dataflow. |
