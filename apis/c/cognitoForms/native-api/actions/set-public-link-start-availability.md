# Set Public Link Start Availability with Cognito Forms

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/public-link-availability`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Set Public Link Start Availability](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/post/forms/{formId}/public-link-availability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Form ID |
| `Start` | body | `date` | yes | Availability start date |
