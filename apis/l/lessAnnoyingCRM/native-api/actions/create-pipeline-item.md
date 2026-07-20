# Create Pipeline Item with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Create Pipeline Item](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items#Goto-CreatePipelineItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactId` | body | `string` | yes | The contact Id this pipeline item will attach to. |
| `PipelineId` | body | `string` | yes | The pipeline Id to add the item to. |
| `StatusId` | body | `string` | yes | The status Id where the item should start. |
| `Note` | body | `string` | no | Optional history note for the pipeline item. |
| `RunStatusAutomation` | body | `boolean` | no | Whether to run the status automation. |
