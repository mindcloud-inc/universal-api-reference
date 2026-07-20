# Upload Client File with CoachAccountable

Uploads a client file to CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Upload Client File](https://www.coachaccountable.com/APIDocs#ClientFile.addAsUpload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client with whom to share this File. |
| `filename` | body | `string` | yes | Maximum length: 300. |
| `title` | body | `string` | no | Maximum length: 200. |
| `folder` | body | `string` | no | Maximum length: 500. |
| `description` | body | `string` | no | Maximum length: 1000. |
| `fileData` | body | `string` | yes | Data of the file to be uploaded, MUST BE Base64 encoded. Maximum length: 5242880. |
