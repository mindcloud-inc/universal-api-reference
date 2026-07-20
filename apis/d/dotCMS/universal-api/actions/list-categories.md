# DotCMS: List Categories

Retrieves category records available in DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-categories?${params}`, {
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
      "entity": [
        {
          "active": true,
          "archived": true,
          "categoryId": "string",
          "categoryName": "Ava Chen",
          "categoryVelocityVarName": "Ava Chen",
          "description": {},
          "idate": "2026-05-07T12:00:00.000Z",
          "iDate": "2026-05-07T12:00:00.000Z",
          "identifier": {},
          "inode": "string",
          "key": "string",
          "keywords": "string",
          "live": true,
          "locked": true,
          "map": {
            "categoryName": "Ava Chen",
            "description": {},
            "inode": "string",
            "key": "string",
            "keywords": "string",
            "sortOrder": 1
          },
          "modDate": "2026-05-07T12:00:00.000Z",
          "modUser": "string",
          "new": true,
          "owner": "string",
          "parentPermissionable": {
            "aliases": "string",
            "archived": true,
            "categoryId": "string",
            "contentTypeId": "string",
            "default": true,
            "dotAsset": true,
            "fileAsset": true,
            "folder": "string",
            "form": true,
            "host": "string",
            "hostname": "Ava Chen",
            "hostThumbnail": {},
            "htmlpage": true,
            "identifier": "string",
            "indexPolicyDependencies": "string",
            "inode": "string",
            "keyValue": true,
            "languageId": 1,
            "languageVariable": true,
            "live": true,
            "locked": true,
            "lowIndexPriority": true,
            "modDate": "2026-05-07T12:00:00.000Z",
            "modUser": "string",
            "name": "Ava Chen",
            "new": true,
            "owner": "string",
            "parent": true,
            "permissionId": "string",
            "permissionType": "string",
            "persona": true,
            "sortOrder": 1,
            "structureInode": "string",
            "systemHost": true,
            "tagStorage": "string",
            "title": "string",
            "titleImage": {},
            "type": "string",
            "vanityUrl": true,
            "variantId": "string",
            "versionId": "string",
            "working": true
          },
          "permissionId": "string",
          "permissionType": "string",
          "sortOrder": 1,
          "title": "string",
          "type": "string",
          "versionId": {},
          "versionType": "string",
          "working": true
        }
      ],
      "pagination": {
        "currentPage": 1,
        "perPage": 1,
        "totalEntries": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity[].active` | boolean |  |
| `entity[].archived` | boolean |  |
| `entity[].categoryId` | string |  |
| `entity[].categoryName` | string |  |
| `entity[].categoryVelocityVarName` | string |  |
| `entity[].description` | object |  |
| `entity[].idate` | date |  |
| `entity[].iDate` | date |  |
| `entity[].identifier` | object |  |
| `entity[].inode` | string |  |
| `entity[].key` | string |  |
| `entity[].keywords` | string |  |
| `entity[].live` | boolean |  |
| `entity[].locked` | boolean |  |
| `entity[].map.categoryName` | string |  |
| `entity[].map.description` | object |  |
| `entity[].map.inode` | string |  |
| `entity[].map.key` | string |  |
| `entity[].map.keywords` | string |  |
| `entity[].map.sortOrder` | number |  |
| `entity[].modDate` | date |  |
| `entity[].modUser` | string |  |
| `entity[].new` | boolean |  |
| `entity[].owner` | string |  |
| `entity[].parentPermissionable.aliases` | string |  |
| `entity[].parentPermissionable.archived` | boolean |  |
| `entity[].parentPermissionable.categoryId` | string |  |
| `entity[].parentPermissionable.contentTypeId` | string |  |
| `entity[].parentPermissionable.default` | boolean |  |
| `entity[].parentPermissionable.dotAsset` | boolean |  |
| `entity[].parentPermissionable.fileAsset` | boolean |  |
| `entity[].parentPermissionable.folder` | string |  |
| `entity[].parentPermissionable.form` | boolean |  |
| `entity[].parentPermissionable.host` | string |  |
| `entity[].parentPermissionable.hostname` | string |  |
| `entity[].parentPermissionable.hostThumbnail` | object |  |
| `entity[].parentPermissionable.htmlpage` | boolean |  |
| `entity[].parentPermissionable.identifier` | string |  |
| `entity[].parentPermissionable.indexPolicyDependencies` | string |  |
| `entity[].parentPermissionable.inode` | string |  |
| `entity[].parentPermissionable.keyValue` | boolean |  |
| `entity[].parentPermissionable.languageId` | number |  |
| `entity[].parentPermissionable.languageVariable` | boolean |  |
| `entity[].parentPermissionable.live` | boolean |  |
| `entity[].parentPermissionable.locked` | boolean |  |
| `entity[].parentPermissionable.lowIndexPriority` | boolean |  |
| `entity[].parentPermissionable.modDate` | date |  |
| `entity[].parentPermissionable.modUser` | string |  |
| `entity[].parentPermissionable.name` | string |  |
| `entity[].parentPermissionable.new` | boolean |  |
| `entity[].parentPermissionable.owner` | string |  |
| `entity[].parentPermissionable.parent` | boolean |  |
| `entity[].parentPermissionable.permissionId` | string |  |
| `entity[].parentPermissionable.permissionType` | string |  |
| `entity[].parentPermissionable.persona` | boolean |  |
| `entity[].parentPermissionable.sortOrder` | number |  |
| `entity[].parentPermissionable.structureInode` | string |  |
| `entity[].parentPermissionable.systemHost` | boolean |  |
| `entity[].parentPermissionable.tagStorage` | string |  |
| `entity[].parentPermissionable.title` | string |  |
| `entity[].parentPermissionable.titleImage` | object |  |
| `entity[].parentPermissionable.type` | string |  |
| `entity[].parentPermissionable.vanityUrl` | boolean |  |
| `entity[].parentPermissionable.variantId` | string |  |
| `entity[].parentPermissionable.versionId` | string |  |
| `entity[].parentPermissionable.working` | boolean |  |
| `entity[].permissionId` | string |  |
| `entity[].permissionType` | string |  |
| `entity[].sortOrder` | number |  |
| `entity[].title` | string |  |
| `entity[].type` | string |  |
| `entity[].versionId` | object |  |
| `entity[].versionType` | string |  |
| `entity[].working` | boolean |  |
| `pagination.currentPage` | number |  |
| `pagination.perPage` | number |  |
| `pagination.totalEntries` | number |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/categories` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

