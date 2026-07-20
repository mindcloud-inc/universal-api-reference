# Google Drive Universal API Examples

These examples use the MindCloud API key and Google Drive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Folders

Lists all Google Drive Folders. Optionally search folders you have access to in a Team Drive.

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

Example response:

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

See the full [List Folders action reference](actions/list-folders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleDrive/latest/actions/list-folders).

## Copy File

Creates a copy of a file in Google Drive.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/copy-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/copy-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "kind": "string",
      "mimeType": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Copy File action reference](actions/copy-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleDrive/latest/actions/copy-file).
