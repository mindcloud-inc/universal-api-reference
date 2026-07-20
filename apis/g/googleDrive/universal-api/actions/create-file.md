# Google Drive: Create File

Creates a new file in Google Drive.

```
POST https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "fileType": "Choose a file type"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "fileType": "Choose a file type"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Give your new File a new Name. |
| `fileType` | list<string> | yes | Choose which Google Workspace file type to create. One of: `document`, `form`, `fusiontable`, `presentation`, `spreadsheet`. Example: `Choose a file type`. |
| `parents` | list<string> | no | The ID of a Google Drive Folder to place your file. When not specified files are added to your My Drive. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `useContentAsIndexableText` | boolean | no | Whether to use the uploaded content as indexable text. Default: `false`. |
| `ignoreDefaultVisibility` | boolean | no | Whether to ignore the domain's default visibility settings for the created file. Domain administrators can choose to make all uploaded files visible to the domain by default; this parameter bypasses that behavior for the request. Permissions are still inherited from parent folders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilities": {
        "canAcceptOwnership": true,
        "canAddChildren": true,
        "canAddMyDriveParent": true,
        "canChangeCopyRequiresWriterPermission": true,
        "canChangeSecurityUpdateEnabled": true,
        "canChangeViewersCanCopyContent": true,
        "canComment": true,
        "canCopy": true,
        "canDelete": true,
        "canDownload": true,
        "canEdit": true,
        "canListChildren": true,
        "canModifyContent": true,
        "canModifyContentRestriction": true,
        "canModifyEditorContentRestriction": true,
        "canModifyLabels": true,
        "canModifyOwnerContentRestriction": true,
        "canMoveChildrenWithinDrive": true,
        "canMoveItemIntoTeamDrive": true,
        "canMoveItemOutOfDrive": true,
        "canMoveItemWithinDrive": true,
        "canReadLabels": true,
        "canReadRevisions": true,
        "canRemoveChildren": true,
        "canRemoveContentRestriction": true,
        "canRemoveMyDriveParent": true,
        "canRename": true,
        "canShare": true,
        "canTrash": true,
        "canUntrash": true
      },
      "copyRequiresWriterPermission": true,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "explicitlyTrashed": true,
      "folderColorRgb": "string",
      "hasThumbnail": true,
      "iconLink": "https://example.com",
      "id": "string",
      "isAppAuthorized": true,
      "kind": "string",
      "lastModifyingUser": {
        "displayName": "Ava Chen",
        "emailAddress": "ava@example.com",
        "kind": "string",
        "me": true,
        "permissionId": "string",
        "photoLink": "https://example.com"
      },
      "linkShareMetadata": {
        "securityUpdateEligible": true,
        "securityUpdateEnabled": true
      },
      "mimeType": "string",
      "modifiedByMe": true,
      "modifiedByMeTime": "2026-05-07T12:00:00.000Z",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "ownedByMe": true,
      "owners": [
        {
          "displayName": "Ava Chen",
          "emailAddress": "ava@example.com",
          "kind": "string",
          "me": true,
          "permissionId": "string",
          "photoLink": "https://example.com"
        }
      ],
      "parents": [
        "string"
      ],
      "permissionIds": [
        "string"
      ],
      "permissions": [
        {
          "deleted": true,
          "displayName": "Ava Chen",
          "emailAddress": "ava@example.com",
          "id": "string",
          "kind": "string",
          "pendingOwner": true,
          "role": "string",
          "type": "string"
        }
      ],
      "quotaBytesUsed": "string",
      "shared": true,
      "spaces": [
        "string"
      ],
      "starred": true,
      "thumbnailVersion": "string",
      "trashed": true,
      "version": "string",
      "viewedByMe": true,
      "viewersCanCopyContent": true,
      "webViewLink": "https://example.com",
      "writersCanShare": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities.canAcceptOwnership` | boolean |  |
| `capabilities.canAddChildren` | boolean |  |
| `capabilities.canAddMyDriveParent` | boolean |  |
| `capabilities.canChangeCopyRequiresWriterPermission` | boolean |  |
| `capabilities.canChangeSecurityUpdateEnabled` | boolean |  |
| `capabilities.canChangeViewersCanCopyContent` | boolean |  |
| `capabilities.canComment` | boolean |  |
| `capabilities.canCopy` | boolean |  |
| `capabilities.canDelete` | boolean |  |
| `capabilities.canDownload` | boolean |  |
| `capabilities.canEdit` | boolean |  |
| `capabilities.canListChildren` | boolean |  |
| `capabilities.canModifyContent` | boolean |  |
| `capabilities.canModifyContentRestriction` | boolean |  |
| `capabilities.canModifyEditorContentRestriction` | boolean |  |
| `capabilities.canModifyLabels` | boolean |  |
| `capabilities.canModifyOwnerContentRestriction` | boolean |  |
| `capabilities.canMoveChildrenWithinDrive` | boolean |  |
| `capabilities.canMoveItemIntoTeamDrive` | boolean |  |
| `capabilities.canMoveItemOutOfDrive` | boolean |  |
| `capabilities.canMoveItemWithinDrive` | boolean |  |
| `capabilities.canReadLabels` | boolean |  |
| `capabilities.canReadRevisions` | boolean |  |
| `capabilities.canRemoveChildren` | boolean |  |
| `capabilities.canRemoveContentRestriction` | boolean |  |
| `capabilities.canRemoveMyDriveParent` | boolean |  |
| `capabilities.canRename` | boolean |  |
| `capabilities.canShare` | boolean |  |
| `capabilities.canTrash` | boolean |  |
| `capabilities.canUntrash` | boolean |  |
| `copyRequiresWriterPermission` | boolean |  |
| `createdTime` | date |  |
| `explicitlyTrashed` | boolean |  |
| `folderColorRgb` | string |  |
| `hasThumbnail` | boolean |  |
| `iconLink` | string |  |
| `id` | string |  |
| `isAppAuthorized` | boolean |  |
| `kind` | string |  |
| `lastModifyingUser.displayName` | string |  |
| `lastModifyingUser.emailAddress` | string |  |
| `lastModifyingUser.kind` | string |  |
| `lastModifyingUser.me` | boolean |  |
| `lastModifyingUser.permissionId` | string |  |
| `lastModifyingUser.photoLink` | string |  |
| `linkShareMetadata.securityUpdateEligible` | boolean |  |
| `linkShareMetadata.securityUpdateEnabled` | boolean |  |
| `mimeType` | string |  |
| `modifiedByMe` | boolean |  |
| `modifiedByMeTime` | date |  |
| `modifiedTime` | date |  |
| `name` | string |  |
| `ownedByMe` | boolean |  |
| `owners[].displayName` | string |  |
| `owners[].emailAddress` | string |  |
| `owners[].kind` | string |  |
| `owners[].me` | boolean |  |
| `owners[].permissionId` | string |  |
| `owners[].photoLink` | string |  |
| `parents[]` | string |  |
| `permissionIds[]` | string |  |
| `permissions[].deleted` | boolean |  |
| `permissions[].displayName` | string |  |
| `permissions[].emailAddress` | string |  |
| `permissions[].id` | string |  |
| `permissions[].kind` | string |  |
| `permissions[].pendingOwner` | boolean |  |
| `permissions[].role` | string |  |
| `permissions[].type` | string |  |
| `quotaBytesUsed` | string |  |
| `shared` | boolean |  |
| `spaces[]` | string |  |
| `starred` | boolean |  |
| `thumbnailVersion` | string |  |
| `trashed` | boolean |  |
| `version` | string |  |
| `viewedByMe` | boolean |  |
| `viewersCanCopyContent` | boolean |  |
| `webViewLink` | string |  |
| `writersCanShare` | boolean |  |

## Native endpoint

Through the native Google Drive API, this operation is `POST /drive/v3/files` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file.md) for the provider-specific parameters and requirements.

