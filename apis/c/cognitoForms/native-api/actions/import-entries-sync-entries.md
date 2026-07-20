# Import Entries Sync Entries with Cognito Forms

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/import-entries`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Import Entries Sync Entries](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/import-entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | yes |
| `Entries` | body | `string` | yes |
