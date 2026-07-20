# Set Public Link Availability with Cognito Forms

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/public-link-availability`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Set Public Link Availability](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/post/forms/{formId}/public-link-availability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Form ID |
| `Start` | body | `date` | no | Availability start date |
| `End` | body | `date` | no | Availability end date |
| `Message` | body | `string` | no | Not Available Message |
