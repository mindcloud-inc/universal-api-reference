# Get Flow Error Summary with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/flows/:flowId/errors`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [Get Flow Error Summary](https://developer.celigo.com/api/api-reference/integrations-and-flows/flows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `list<string>` | yes | Flow to summarize open errors for, per step. |
| `_toolImportId` | query | `string` | no | Summarize the tool chain of this ToolImport step instead of the flow steps. |
