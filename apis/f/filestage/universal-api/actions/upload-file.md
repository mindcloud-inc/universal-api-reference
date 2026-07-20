# Filestage: Upload File

Creates a new file in Filestage from a URL.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileURL": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileURL": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileURL` | string | yes | A URL where the file can be downloaded. Our server will perform a GET request to this URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stepIds[]` | array<string> | no | Array of step IDs. This is only required if the `projectId` is empty |
| `projectId` | string | no | The ID of the project to upload the file to. This field is required when the `stepIds` field is empty |
| `fileId` | string | no | The ID of the file that gets new version. |
| `fileHeaders` | object | no | A key-value map of HTTP headers to include in the GET request to the `fileURL`. You can use this to provide authentication tokens (e.g., `Authorization: Bearer <token>`) if the URL is protected or other headers neccessary to make the GET request to the `fileUrl` successful. |
| `callbackURL` | string | no | The URL where we will send a POST request to notify you of the upload's final status. This URL must be publicly accessible. |
| `callbackHeaders` | object | no | A key-value map of HTTP headers to include in the POST request to your `callbackURL`. Use this for security, such as including a pre-shared secret or auth token. |
| `fileName` | string | no | The desired name for the file, including its extension (e.g., `document.pdf`). If omitted, the name will be inferred. |
| `uploaderEmail` | string | no | The email address of the user you want to upload the file on behalf of. This user will be displayed as the file uploader. |
| `sectionId` | string | no | The ID of a specific section within a project to organize the file into. If omitted, the file is placed in the default section. |
| `pregeneratedFileId` | string | no | `pregeneratedFileId` in the response body of `POST /files/upload-url` |
| `externalId` | string | no | A custom identifier from your system to associate with the file, useful for cross-referencing. **Note:** We do not enforce uniqueness on this field; it is your responsibility to manage it. |
| `externalMetadata` | object | no | Custom data that could be associated with the File. `externalMetadata` field cannot exceed 10Kb of data size and also a maximum of 5 object properties are allowed in this object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileId": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileId` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `POST /files` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

