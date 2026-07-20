# Wrike: Create Folder

Creates a new folder in a Wrike folder.

```
POST https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Wrike parent folder ID where the folder will be created. |
| `title` | string | yes | Title, cannot be empty |
| `description` | string | no | Folder description |
| `shareds` | string | no | User or invitation IDs to share with, as a JSON string array |
| `metadata` | string | no | Metadata entries as a JSON string array |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields` | string | no | Custom field values as a JSON string array |
| `customColumns` | string | no | Custom field IDs as a JSON string array |
| `project` | string | no | Project settings as a JSON object string |
| `userAccessRoles` | string | no | User ID for access role assignment |
| `withInvitations` | boolean | no | Include invitations in owner and shared lists |
| `customItemTypeId` | string | no | Custom item type ID to create a project from |
| `plainTextCustomFields` | boolean | no | Strip HTML tags from custom fields |
| `fields` | string | no | Response field names as a JSON string array |

## Response

```json
{
  "success": true,
  "data": [
    {
      "childIds": [
        "string"
      ],
      "color": "string",
      "customItemTypeId": "string",
      "id": "string",
      "project": {},
      "scope": "string",
      "space": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childIds` | array<string> |  |
| `color` | string |  |
| `customItemTypeId` | string |  |
| `id` | string |  |
| `project` | object |  |
| `scope` | string |  |
| `space` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Wrike API, this operation is `POST /folders/:folderId/folders` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

