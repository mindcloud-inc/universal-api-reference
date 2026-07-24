# Create Pipeline Stage with HubSpot

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/pipelines/:objectType/:pipelineId/stages`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Pipeline Stage](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipeline-stages/post-crm-v3-pipelines-objectType-pipelineId-stages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The CRM object type whose pipeline will receive the new stage. Use `deals` for deal stages. |
| `pipelineId` | path | `string` | yes | The ID of the pipeline that should receive the new stage. |
| `label` | body | `string` | yes | The name of the stage as it is displayed in HubSpot. The label must be unique within the pipeline. |
| `displayOrder` | body | `number` | yes | The order of the stage in the pipeline. If multiple stages share the same order, HubSpot sorts them alphabetically by label. |
| `metadata` | body | `object` | no | Additional stage metadata. For deal stages, HubSpot requires `probability` inside this object. |
| `metadata.probability` | body | `string` | yes | For deal stages, the required close probability from `0.0` to `1.0`, where `0.0` is Closed Lost and `1.0` is Closed Won. |
