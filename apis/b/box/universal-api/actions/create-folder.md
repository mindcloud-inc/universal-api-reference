# Box: Create Folder



```
POST https://connect.mindcloud.co/v1/universal/box/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/box/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Codex Box Test Folder",
  "parentFolderId": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/box/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Codex Box Test Folder",
    "parentFolderId": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the new folder. Example: `Codex Box Test Folder`. |
| `parentFolderId` | string | yes | Parent Box folder ID. Use `0` to create the folder in the root folder. Default: `0`. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional comma-separated list of folder fields to include in the response. Example: `id,type,name,parent,path_collection`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentCreatedAt": "string",
      "contentModifiedAt": "string",
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "description": "string",
      "etag": "string",
      "folderUploadEmail": {},
      "id": "string",
      "itemCollection": {
        "limit": 1,
        "offset": 1,
        "order": [
          {
            "by": "string",
            "direction": "string"
          }
        ],
        "totalCount": 1
      },
      "itemStatus": "string",
      "modifiedAt": "string",
      "modifiedBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "name": "Ava Chen",
      "ownedBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "parent": {
        "etag": {},
        "id": "string",
        "name": "Ava Chen",
        "sequenceId": {},
        "type": "string"
      },
      "pathCollection": {
        "entries": [
          {
            "etag": {},
            "id": "string",
            "name": "Ava Chen",
            "sequenceId": {},
            "type": "string"
          }
        ],
        "totalCount": 1
      },
      "purgedAt": {},
      "sequenceId": "string",
      "sharedLink": {},
      "size": 1,
      "trashedAt": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentCreatedAt` | string |  |
| `contentModifiedAt` | string |  |
| `createdAt` | string |  |
| `createdBy.id` | string |  |
| `createdBy.login` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `description` | string |  |
| `etag` | string |  |
| `folderUploadEmail` | object |  |
| `id` | string |  |
| `itemCollection.limit` | number |  |
| `itemCollection.offset` | number |  |
| `itemCollection.order[].by` | string |  |
| `itemCollection.order[].direction` | string |  |
| `itemCollection.totalCount` | number |  |
| `itemStatus` | string |  |
| `modifiedAt` | string |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.login` | string |  |
| `modifiedBy.name` | string |  |
| `modifiedBy.type` | string |  |
| `name` | string |  |
| `ownedBy.id` | string |  |
| `ownedBy.login` | string |  |
| `ownedBy.name` | string |  |
| `ownedBy.type` | string |  |
| `parent.etag` | object |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `parent.sequenceId` | object |  |
| `parent.type` | string |  |
| `pathCollection.entries[].etag` | object |  |
| `pathCollection.entries[].id` | string |  |
| `pathCollection.entries[].name` | string |  |
| `pathCollection.entries[].sequenceId` | object |  |
| `pathCollection.entries[].type` | string |  |
| `pathCollection.totalCount` | number |  |
| `purgedAt` | object |  |
| `sequenceId` | string |  |
| `sharedLink` | object |  |
| `size` | number |  |
| `trashedAt` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Box API, this operation is `POST /folders` (base URL `https://api.box.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

