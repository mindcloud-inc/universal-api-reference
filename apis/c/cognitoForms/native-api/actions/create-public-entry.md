# Create Public Entry with Cognito Forms

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/entries`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Create Public Entry](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The ID of the Form for which you want to create an Entry |
| `Entry.Action` | body | `string` | no | Entry action. Allowed values: Submit, Update. |
| `Entry.Role` | body | `string` | no | Entry role. Allowed values: Public, Internal, Reviewer. |
