# Update Entry As Internal with Cognito Forms

## Endpoint

- **Method:** `PATCH`
- **Path:** `/forms/:formId/entries/:entryId`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Update Entry As Internal](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/patch/forms/{formId}/entries/{entryId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The ID of the Form for which you want to update an Entry |
| `entryId` | path | `string` | yes | The ID of the Entry you want to update |
| `Entry.Action` | body | `string` | no | Entry action. Allowed values: Submit, Update. |
| `Entry.Role` | body | `string` | no | Entry role. Allowed values: Public, Internal, Reviewer. |
