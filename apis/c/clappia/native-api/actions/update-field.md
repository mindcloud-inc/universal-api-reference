# Update Field with Clappia

Updates an existing app field in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/updateField`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Field](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `fieldName` | body | `string` | yes | Current variable name of the field to update. |
| `newFieldName` | body | `string` | no | Optional new variable name for the field. |
| `label` | body | `string` | no | Updated field label. |
| `description` | body | `string` | no | Updated helper text for the field. |
| `required` | body | `boolean` | no | Whether the field must be filled in. |
| `blockWidthPercentageDesktop` | body | `number` | no | Updated desktop width percentage for the field block. |
| `blockWidthPercentageMobile` | body | `number` | no | Updated mobile width percentage for the field block. |
| `validation` | body | `string` | no | Updated validation mode for the field. |
| `isEditable` | body | `boolean` | no | Whether users can edit the field after the update. |
