# List View Entries Select Fields with Cognito Forms

## Endpoint

- **Method:** `GET`
- **Path:** `/odata/Forms(:formId)/Views(:viewId)/Entries`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [List View Entries Select Fields](https://www.cognitoforms.com/support/496/data-integration/cognito-forms-api/odata-reference#tag/entries/get/Forms({formId})/Views({viewId})/Entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | yes |
| `viewId` | path | `string` | yes |
| `$select` | query | `string` | no |
