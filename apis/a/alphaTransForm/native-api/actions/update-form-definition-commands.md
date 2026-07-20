# Update Form Definition Commands with Alpha TransForm

Updates form definition commands in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/UpdateFormDefinitionCommandsForFormId/:formId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Update Form Definition Commands](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/UpdateFormDefinitionCommandsForFormId.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Form definition id. |
| `formdefinitioncommandsjson[]` | body | `array<object>` | no | JSON array of form definition commands. Send multiple values as a array. |
