# Dropbox: Create Folder

Creates a new folder in Dropbox.

```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Path in Dropbox where the folder should be created. Example: `/MindCloud Dropbox Test/dropbox-stage3-20260306-171004`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autorename` | boolean | no | If true, Dropbox tries to rename the folder when the target path conflicts. Default: `false`. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "pathDisplay": "string",
      "pathLower": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `pathDisplay` | string |  |
| `pathLower` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /files/create_folder_v2` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

