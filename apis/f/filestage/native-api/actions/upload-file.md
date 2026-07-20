# Upload File with Filestage

Creates a new file in Filestage from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Upload File](https://developers.filestage.io/docs/api/1wmibjt5eccjb-upload-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stepIds[]` | body | `array<string>` | no | Array of step IDs. This is only required if the `projectId` is empty |
| `projectId` | body | `string` | no | The ID of the project to upload the file to. This field is required when the `stepIds` field is empty |
| `fileId` | body | `string` | no | The ID of the file that gets new version. |
| `fileURL` | body | `string` | yes | A URL where the file can be downloaded. Our server will perform a GET request to this URL. |
| `fileHeaders` | body | `object` | no | A key-value map of HTTP headers to include in the GET request to the `fileURL`. You can use this to provide authentication tokens (e.g., `Authorization: Bearer <token>`) if the URL is protected or other headers neccessary to make the GET request to the `fileUrl` successful. |
| `callbackURL` | body | `string` | no | The URL where we will send a POST request to notify you of the upload's final status. This URL must be publicly accessible. |
| `callbackHeaders` | body | `object` | no | A key-value map of HTTP headers to include in the POST request to your `callbackURL`. Use this for security, such as including a pre-shared secret or auth token. |
| `fileName` | body | `string` | no | The desired name for the file, including its extension (e.g., `document.pdf`). If omitted, the name will be inferred. |
| `uploaderEmail` | body | `string` | no | The email address of the user you want to upload the file on behalf of. This user will be displayed as the file uploader. |
| `sectionId` | body | `string` | no | The ID of a specific section within a project to organize the file into. If omitted, the file is placed in the default section. |
| `pregeneratedFileId` | body | `string` | no | `pregeneratedFileId` in the response body of `POST /files/upload-url` |
| `externalId` | body | `string` | no | A custom identifier from your system to associate with the file, useful for cross-referencing. **Note:** We do not enforce uniqueness on this field; it is your responsibility to manage it. |
| `externalMetadata` | body | `object` | no | Custom data that could be associated with the File. `externalMetadata` field cannot exceed 10Kb of data size and also a maximum of 5 object properties are allowed in this object. |
