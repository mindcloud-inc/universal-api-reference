# Get Form Input Schema with Cognito Forms

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/schema`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Get Form Input Schema](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/get/forms/{formId}/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The ID of the Form |
| `includeLinks` | query | `boolean` | no | Determines whether links should be included in the schema |
