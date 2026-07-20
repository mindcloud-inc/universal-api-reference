# Google Drive: List Folders

Lists all Google Drive Folders. Optionally search folders you have access to in a Team Drive.

```
GET https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/list-folders?${params}`, {
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
| `q` | string | no | Search for folders based on specific parameters. Uses `q` param. See more here: https://developers.google.com/drive/api/guides/search-files |
| `orderBy` | list<string> | no | Choose one or multiple order options to sort the results. |

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
      "permissionIds": [
        "string"
      ],
      "permissions": [
        {
          "allowFileDiscovery": true,
          "id": "string",
          "kind": "string",
          "role": "string",
          "type": "string"
        }
      ],
      "quotaBytesUsed": "string",
      "shared": true,
      "sharedWithMeTime": "2026-05-07T12:00:00.000Z",
      "spaces": [
        "string"
      ],
      "starred": true,
      "thumbnailVersion": "string",
      "trashed": true,
      "version": "string",
      "viewedByMe": true,
      "viewedByMeTime": "2026-05-07T12:00:00.000Z",
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
| `modifiedTime` | date |  |
| `name` | string |  |
| `ownedByMe` | boolean |  |
| `owners[].displayName` | string |  |
| `owners[].emailAddress` | string |  |
| `owners[].kind` | string |  |
| `owners[].me` | boolean |  |
| `owners[].permissionId` | string |  |
| `owners[].photoLink` | string |  |
| `permissionIds[]` | string |  |
| `permissions[].allowFileDiscovery` | boolean |  |
| `permissions[].id` | string |  |
| `permissions[].kind` | string |  |
| `permissions[].role` | string |  |
| `permissions[].type` | string |  |
| `quotaBytesUsed` | string |  |
| `shared` | boolean |  |
| `sharedWithMeTime` | date |  |
| `spaces[]` | string |  |
| `starred` | boolean |  |
| `thumbnailVersion` | string |  |
| `trashed` | boolean |  |
| `version` | string |  |
| `viewedByMe` | boolean |  |
| `viewedByMeTime` | date |  |
| `viewersCanCopyContent` | boolean |  |
| `webViewLink` | string |  |
| `writersCanShare` | boolean |  |

## Native endpoint

Through the native Google Drive API, this operation is `GET /drive/v3/files` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

