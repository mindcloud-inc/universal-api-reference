# Upload File with Cognito Forms

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://www.cognitoforms.com/api`
- **Official documentation:** [Upload File](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `File` | body | `string` | yes | The file to upload (multipart/form-data). |
