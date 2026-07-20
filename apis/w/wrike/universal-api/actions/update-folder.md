# Wrike: Update Folder

Updates an existing folder in Wrike.

```
PUT https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Wrike folder ID. |
| `title` | string | no | Title |
| `description` | string | no | Folder description |
| `addParents` | string | no | Folder IDs to add as parents, as a JSON string array |
| `removeParents` | string | no | Folder IDs to remove as parents, as a JSON string array |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addShareds` | string | no | User or invitation IDs to share with, as a JSON string array |
| `removeShareds` | string | no | User or invitation IDs to unshare, as a JSON string array |
| `metadata` | string | no | Metadata entries to update, as a JSON string array |
| `restore` | boolean | no | Restore folder from recycled bin |
| `customFields` | string | no | Custom field values to update, as a JSON string array |
| `customColumns` | string | no | Custom field IDs as a JSON string array |
| `clearCustomColumns` | boolean | no | Remove all custom fields associated with the folder |
| `project` | string | no | Project settings as a JSON object string |
| `addAccessRoles` | string | no | User ID for access role assignment |
| `removeAccessRoles` | string | no | User IDs whose access roles should be removed, as a JSON string array |
| `withInvitations` | boolean | no | Include invitations in owner and shared lists |
| `convertToCustomItemType` | string | no | Custom item type ID |
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

Through the native Wrike API, this operation is `PUT /folders/:folderId` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder.md) for the provider-specific parameters and requirements.

