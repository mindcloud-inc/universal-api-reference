# DotCMS: Get Current Site

Retrieves the current site from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-current-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-current-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-current-site?${params}`, {
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
      "entity": {
        "aliases": "string",
        "archived": true,
        "categoryId": "string",
        "contentTypeId": "string",
        "default": true,
        "dotAsset": true,
        "fileAsset": true,
        "folder": true,
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
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity.aliases` | string |  |
| `entity.archived` | boolean |  |
| `entity.categoryId` | string |  |
| `entity.contentTypeId` | string |  |
| `entity.default` | boolean |  |
| `entity.dotAsset` | boolean |  |
| `entity.fileAsset` | boolean |  |
| `entity.folder` | boolean |  |
| `entity.form` | boolean |  |
| `entity.host` | string |  |
| `entity.hostname` | string |  |
| `entity.hostThumbnail` | object |  |
| `entity.htmlpage` | boolean |  |
| `entity.identifier` | string |  |
| `entity.indexPolicyDependencies` | string |  |
| `entity.inode` | string |  |
| `entity.keyValue` | boolean |  |
| `entity.languageId` | number |  |
| `entity.languageVariable` | boolean |  |
| `entity.live` | boolean |  |
| `entity.locked` | boolean |  |
| `entity.lowIndexPriority` | boolean |  |
| `entity.modDate` | date |  |
| `entity.modUser` | string |  |
| `entity.name` | string |  |
| `entity.new` | boolean |  |
| `entity.owner` | string |  |
| `entity.parent` | boolean |  |
| `entity.permissionId` | string |  |
| `entity.permissionType` | string |  |
| `entity.persona` | boolean |  |
| `entity.sortOrder` | number |  |
| `entity.structureInode` | string |  |
| `entity.systemHost` | boolean |  |
| `entity.tagStorage` | string |  |
| `entity.title` | string |  |
| `entity.titleImage` | object |  |
| `entity.type` | string |  |
| `entity.vanityUrl` | boolean |  |
| `entity.variantId` | string |  |
| `entity.versionId` | string |  |
| `entity.working` | boolean |  |
| `pagination` | object |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/site/currentSite` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-site.md) for the provider-specific parameters and requirements.

