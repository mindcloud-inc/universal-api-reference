# Canva: Create Folder

Creates a new folder in Canva.

```
POST https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "My awesome holiday",
  "parentFolderId": "root"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "My awesome holiday",
    "parentFolderId": "root"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the folder. Example: `My awesome holiday`. |
| `parentFolderId` | string | yes | The folder ID of the parent folder. Use root for top-level projects or uploads for the Uploads folder. Example: `root`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {
        "createdAt": 1,
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | object |  |
| `folder.createdAt` | number |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `folder.updatedAt` | number |  |

## Native endpoint

Through the native Canva API, this operation is `POST /v1/folders` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

