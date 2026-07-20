# Get Entry with Cognito Forms

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/entries/:entryId`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Get Entry](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/get/forms/{formId}/entries/{entryId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The ID of the Form for which you want to retrieve an Entry |
| `entryId` | path | `string` | yes | The ID of the Entry you want to retrieve |
