# Cloudinary: Delete Folder

Deletes a folder from your Cloudinary account.

```
DELETE https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-folder?connectionId=$CONNECTION_ID&folder=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folder": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-folder?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folder` | string | yes | The full path of the empty folder to delete. |
| `skipBackup` | boolean | no | When true, also deletes the folder from backup storage. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | array<string> | The folder paths deleted by the request. |

## Native endpoint

Through the native Cloudinary API, this operation is `DELETE /folders/:folder` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-folder.md) for the provider-specific parameters and requirements.

