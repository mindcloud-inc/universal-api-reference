# Set Publish Settings with Google Forms

Updates a form's publish settings in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:setPublishSettings`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Set Publish Settings](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/setPublishSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `publishState` | body | `list` | yes | Publish or unpublish the form. Accepted values: `0`, `1`. |
| `acceptingResponses` | body | `boolean` | no | Whether the published form accepts responses. |
| `updateMask` | body | `string` | no | Advanced: publish settings field mask. Defaults to publishState. |
