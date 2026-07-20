# List Pipelines with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [List Pipelines](https://account.lessannoyingcrm.com/api_docs/v2/Settings_Functions/Pipelines#Goto-GetPipelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IncludeArchivedPipelines` | body | `boolean` | no | Whether to include archived pipelines. |
| `IncludeCustomFields` | body | `boolean` | no | Whether to include custom field metadata. |
| `IncludeHiddenPipelines` | body | `boolean` | no | Whether admins should include hidden pipelines. |
