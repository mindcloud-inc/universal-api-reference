# Update Pipeline Item with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Update Pipeline Item](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items#Goto-EditPipelineItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PipelineItemId` | body | `string` | yes | The pipeline item Id to update. |
| `StatusId` | body | `string` | no | Updated status Id for the item. |
| `Note` | body | `string` | no | Optional history note for the status change. |
| `RunStatusAutomation` | body | `boolean` | no | Whether to run the status automation. |
