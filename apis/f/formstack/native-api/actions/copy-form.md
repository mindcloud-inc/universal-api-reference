# Copy Form with Formstack

Creates a copy of a form in Formstack.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/copy`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Copy Form](https://developers.formstack.com/reference/copyform-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<number>` | yes | The ID of the form. |
| `includeIntegrations` | query | `boolean` | no | Whether to copy integrations. |
| `includeEmails` | query | `boolean` | no | Whether to copy emails. |
| `template` | query | `number` | no | ID of template to use when copying. |
| `folder` | query | `number` | no | ID of folder where the copy should be saved. |
