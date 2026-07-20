# ONLYOFFICE DocSpace: Get My Documents Section

Retrieves your My Documents section from ONLYOFFICE DocSpace.

```
GET https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-my-documents-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ONLYOFFICE DocSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-my-documents-section?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-my-documents-section?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "current": {
        "access": 1,
        "availableShareRights": {
          "externalLink": [
            "https://example.com"
          ],
          "group": [
            "string"
          ],
          "primaryExternalLink": [
            "https://example.com"
          ],
          "user": [
            "string"
          ]
        },
        "canShare": true,
        "created": "2026-05-07T12:00:00.000Z",
        "createdBy": {
          "avatar": "string",
          "avatarMax": "string",
          "avatarMedium": "string",
          "avatarOriginal": "string",
          "avatarSmall": "string",
          "displayName": "Ava Chen",
          "hasAvatar": true,
          "id": "string",
          "isAnonim": true,
          "profileUrl": "https://example.com"
        },
        "denyDownload": true,
        "fileEntryType": 1,
        "filesCount": 1,
        "foldersCount": 1,
        "id": 1,
        "indexing": true,
        "mute": true,
        "new": 1,
        "parentId": 1,
        "parentShared": true,
        "pinned": true,
        "private": true,
        "rootFolderId": 1,
        "rootFolderType": 1,
        "security": {
          "changeOwner": true,
          "copy": true,
          "copyLink": true,
          "copySharedLink": true,
          "copyTo": true,
          "create": true,
          "createRoomFrom": true,
          "delete": true,
          "download": true,
          "duplicate": true,
          "editAccess": true,
          "editRoom": true,
          "embed": true,
          "indexExport": true,
          "move": true,
          "moveTo": true,
          "mute": true,
          "pin": true,
          "read": true,
          "reconnect": true,
          "rename": true,
          "useChat": true
        },
        "shared": true,
        "sharedForUser": true,
        "shortWebUrl": "https://example.com",
        "title": "string",
        "updated": "2026-05-07T12:00:00.000Z",
        "updatedBy": {
          "avatar": "string",
          "avatarMax": "string",
          "avatarMedium": "string",
          "avatarOriginal": "string",
          "avatarSmall": "string",
          "displayName": "Ava Chen",
          "hasAvatar": true,
          "id": "string",
          "isAnonim": true,
          "profileUrl": "https://example.com"
        }
      },
      "files": [
        {
          "access": 1,
          "availableShareRights": {
            "externalLink": [
              "https://example.com"
            ],
            "group": [
              "string"
            ],
            "primaryExternalLink": [
              "https://example.com"
            ],
            "user": [
              "string"
            ]
          },
          "canShare": true,
          "comment": "string",
          "contentLength": "string",
          "created": "2026-05-07T12:00:00.000Z",
          "createdBy": {
            "avatar": "string",
            "avatarMax": "string",
            "avatarMedium": "string",
            "avatarOriginal": "string",
            "avatarSmall": "string",
            "displayName": "Ava Chen",
            "hasAvatar": true,
            "id": "string",
            "isAnonim": true,
            "profileUrl": "https://example.com"
          },
          "fileEntryType": 1,
          "fileExst": "string",
          "fileStatus": 1,
          "fileType": 1,
          "folderId": 1,
          "formFillingStatus": 1,
          "id": 1,
          "mute": true,
          "parentShared": true,
          "pureContentLength": 1,
          "rootFolderId": 1,
          "rootFolderType": 1,
          "security": {
            "askAi": true,
            "comment": true,
            "convert": true,
            "copy": true,
            "copyLink": true,
            "createRoomFrom": true,
            "customFilter": true,
            "delete": true,
            "download": true,
            "duplicate": true,
            "edit": true,
            "editHistory": true,
            "embed": true,
            "fillForms": true,
            "fillingStatus": true,
            "lock": true,
            "move": true,
            "openForm": true,
            "read": true,
            "readHistory": true,
            "rename": true,
            "resetFilling": true,
            "review": true,
            "startFilling": true,
            "stopFilling": true,
            "submitToFormGallery": true,
            "vectorization": true
          },
          "shared": true,
          "sharedForUser": true,
          "shareSettings": {
            "externalLink": 1
          },
          "shortWebUrl": "https://example.com",
          "thumbnailStatus": 1,
          "title": "string",
          "updated": "2026-05-07T12:00:00.000Z",
          "updatedBy": {
            "avatar": "string",
            "avatarMax": "string",
            "avatarMedium": "string",
            "avatarOriginal": "string",
            "avatarSmall": "string",
            "displayName": "Ava Chen",
            "hasAvatar": true,
            "id": "string",
            "isAnonim": true,
            "profileUrl": "https://example.com"
          },
          "version": 1,
          "versionGroup": 1,
          "viewAccessibility": {
            "canConvert": true,
            "imageView": true,
            "mediaView": true,
            "mustConvert": true,
            "webComment": true,
            "webCustomFilterEditing": true,
            "webEdit": true,
            "webRestrictedEditing": true,
            "webReview": true,
            "webView": true
          },
          "viewUrl": "https://example.com",
          "webUrl": "https://example.com"
        }
      ],
      "new": 1,
      "pathParts": [
        {
          "folderType": 1,
          "id": 1,
          "title": "string"
        }
      ],
      "startIndex": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `current.access` | number |  |
| `current.availableShareRights.externalLink[]` | string |  |
| `current.availableShareRights.group[]` | string |  |
| `current.availableShareRights.primaryExternalLink[]` | string |  |
| `current.availableShareRights.user[]` | string |  |
| `current.canShare` | boolean |  |
| `current.created` | date |  |
| `current.createdBy.avatar` | string |  |
| `current.createdBy.avatarMax` | string |  |
| `current.createdBy.avatarMedium` | string |  |
| `current.createdBy.avatarOriginal` | string |  |
| `current.createdBy.avatarSmall` | string |  |
| `current.createdBy.displayName` | string |  |
| `current.createdBy.hasAvatar` | boolean |  |
| `current.createdBy.id` | string |  |
| `current.createdBy.isAnonim` | boolean |  |
| `current.createdBy.profileUrl` | string |  |
| `current.denyDownload` | boolean |  |
| `current.fileEntryType` | number |  |
| `current.filesCount` | number |  |
| `current.foldersCount` | number |  |
| `current.id` | number |  |
| `current.indexing` | boolean |  |
| `current.mute` | boolean |  |
| `current.new` | number |  |
| `current.parentId` | number |  |
| `current.parentShared` | boolean |  |
| `current.pinned` | boolean |  |
| `current.private` | boolean |  |
| `current.rootFolderId` | number |  |
| `current.rootFolderType` | number |  |
| `current.security.changeOwner` | boolean |  |
| `current.security.copy` | boolean |  |
| `current.security.copyLink` | boolean |  |
| `current.security.copySharedLink` | boolean |  |
| `current.security.copyTo` | boolean |  |
| `current.security.create` | boolean |  |
| `current.security.createRoomFrom` | boolean |  |
| `current.security.delete` | boolean |  |
| `current.security.download` | boolean |  |
| `current.security.duplicate` | boolean |  |
| `current.security.editAccess` | boolean |  |
| `current.security.editRoom` | boolean |  |
| `current.security.embed` | boolean |  |
| `current.security.indexExport` | boolean |  |
| `current.security.move` | boolean |  |
| `current.security.moveTo` | boolean |  |
| `current.security.mute` | boolean |  |
| `current.security.pin` | boolean |  |
| `current.security.read` | boolean |  |
| `current.security.reconnect` | boolean |  |
| `current.security.rename` | boolean |  |
| `current.security.useChat` | boolean |  |
| `current.shared` | boolean |  |
| `current.sharedForUser` | boolean |  |
| `current.shortWebUrl` | string |  |
| `current.title` | string |  |
| `current.updated` | date |  |
| `current.updatedBy.avatar` | string |  |
| `current.updatedBy.avatarMax` | string |  |
| `current.updatedBy.avatarMedium` | string |  |
| `current.updatedBy.avatarOriginal` | string |  |
| `current.updatedBy.avatarSmall` | string |  |
| `current.updatedBy.displayName` | string |  |
| `current.updatedBy.hasAvatar` | boolean |  |
| `current.updatedBy.id` | string |  |
| `current.updatedBy.isAnonim` | boolean |  |
| `current.updatedBy.profileUrl` | string |  |
| `files[].access` | number |  |
| `files[].availableShareRights.externalLink[]` | string |  |
| `files[].availableShareRights.group[]` | string |  |
| `files[].availableShareRights.primaryExternalLink[]` | string |  |
| `files[].availableShareRights.user[]` | string |  |
| `files[].canShare` | boolean |  |
| `files[].comment` | string |  |
| `files[].contentLength` | string |  |
| `files[].created` | date |  |
| `files[].createdBy.avatar` | string |  |
| `files[].createdBy.avatarMax` | string |  |
| `files[].createdBy.avatarMedium` | string |  |
| `files[].createdBy.avatarOriginal` | string |  |
| `files[].createdBy.avatarSmall` | string |  |
| `files[].createdBy.displayName` | string |  |
| `files[].createdBy.hasAvatar` | boolean |  |
| `files[].createdBy.id` | string |  |
| `files[].createdBy.isAnonim` | boolean |  |
| `files[].createdBy.profileUrl` | string |  |
| `files[].fileEntryType` | number |  |
| `files[].fileExst` | string |  |
| `files[].fileStatus` | number |  |
| `files[].fileType` | number |  |
| `files[].folderId` | number |  |
| `files[].formFillingStatus` | number |  |
| `files[].id` | number |  |
| `files[].mute` | boolean |  |
| `files[].parentShared` | boolean |  |
| `files[].pureContentLength` | number |  |
| `files[].rootFolderId` | number |  |
| `files[].rootFolderType` | number |  |
| `files[].security.askAi` | boolean |  |
| `files[].security.comment` | boolean |  |
| `files[].security.convert` | boolean |  |
| `files[].security.copy` | boolean |  |
| `files[].security.copyLink` | boolean |  |
| `files[].security.createRoomFrom` | boolean |  |
| `files[].security.customFilter` | boolean |  |
| `files[].security.delete` | boolean |  |
| `files[].security.download` | boolean |  |
| `files[].security.duplicate` | boolean |  |
| `files[].security.edit` | boolean |  |
| `files[].security.editHistory` | boolean |  |
| `files[].security.embed` | boolean |  |
| `files[].security.fillForms` | boolean |  |
| `files[].security.fillingStatus` | boolean |  |
| `files[].security.lock` | boolean |  |
| `files[].security.move` | boolean |  |
| `files[].security.openForm` | boolean |  |
| `files[].security.read` | boolean |  |
| `files[].security.readHistory` | boolean |  |
| `files[].security.rename` | boolean |  |
| `files[].security.resetFilling` | boolean |  |
| `files[].security.review` | boolean |  |
| `files[].security.startFilling` | boolean |  |
| `files[].security.stopFilling` | boolean |  |
| `files[].security.submitToFormGallery` | boolean |  |
| `files[].security.vectorization` | boolean |  |
| `files[].shared` | boolean |  |
| `files[].sharedForUser` | boolean |  |
| `files[].shareSettings.externalLink` | number |  |
| `files[].shortWebUrl` | string |  |
| `files[].thumbnailStatus` | number |  |
| `files[].title` | string |  |
| `files[].updated` | date |  |
| `files[].updatedBy.avatar` | string |  |
| `files[].updatedBy.avatarMax` | string |  |
| `files[].updatedBy.avatarMedium` | string |  |
| `files[].updatedBy.avatarOriginal` | string |  |
| `files[].updatedBy.avatarSmall` | string |  |
| `files[].updatedBy.displayName` | string |  |
| `files[].updatedBy.hasAvatar` | boolean |  |
| `files[].updatedBy.id` | string |  |
| `files[].updatedBy.isAnonim` | boolean |  |
| `files[].updatedBy.profileUrl` | string |  |
| `files[].version` | number |  |
| `files[].versionGroup` | number |  |
| `files[].viewAccessibility.canConvert` | boolean |  |
| `files[].viewAccessibility.imageView` | boolean |  |
| `files[].viewAccessibility.mediaView` | boolean |  |
| `files[].viewAccessibility.mustConvert` | boolean |  |
| `files[].viewAccessibility.webComment` | boolean |  |
| `files[].viewAccessibility.webCustomFilterEditing` | boolean |  |
| `files[].viewAccessibility.webEdit` | boolean |  |
| `files[].viewAccessibility.webRestrictedEditing` | boolean |  |
| `files[].viewAccessibility.webReview` | boolean |  |
| `files[].viewAccessibility.webView` | boolean |  |
| `files[].viewUrl` | string |  |
| `files[].webUrl` | string |  |
| `new` | number |  |
| `pathParts[].folderType` | number |  |
| `pathParts[].id` | number |  |
| `pathParts[].title` | string |  |
| `startIndex` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ONLYOFFICE DocSpace API, this operation is `GET /api/2.0/files/@my` (base URL `https://docspace-t0dtrp.onlyoffice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-documents-section.md) for the provider-specific parameters and requirements.

