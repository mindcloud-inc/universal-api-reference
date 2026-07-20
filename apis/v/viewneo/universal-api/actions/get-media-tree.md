# Viewneo: Get Media Tree

Retrieves the media tree from Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-media-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-media-tree?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-media-tree?${params}`, {
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
      "attachableId": {},
      "attachableType": {},
      "companyId": 1,
      "id": 1,
      "isDefault": true,
      "isDemo": true,
      "isHidden": true,
      "isLocked": true,
      "isShared": true,
      "name": "Ava Chen",
      "nodes": [
        {
          "attachableId": {},
          "attachableType": {},
          "companyId": 1,
          "createdAt": "string",
          "deletedAt": {},
          "id": 1,
          "isDefault": 1,
          "isDemo": 1,
          "isHidden": 1,
          "isLocked": 1,
          "isShared": 1,
          "mediaFileIdAsParentDirectory": {},
          "name": "Ava Chen",
          "nodes": [
            {
              "attachableId": {},
              "attachableType": {},
              "companyId": 1,
              "createdAt": "string",
              "deletedAt": {},
              "id": 1,
              "isDefault": 1,
              "isDemo": 1,
              "isHidden": 1,
              "isLocked": 1,
              "isShared": 1,
              "mediaFileIdAsParentDirectory": 1,
              "name": "Ava Chen",
              "status": {},
              "thumbnailExtension": {},
              "thumbnailHash": {},
              "thumbnailMimeType": {},
              "type": 1,
              "updatedAt": "string"
            }
          ],
          "status": {},
          "thumbnailExtension": {},
          "thumbnailHash": {},
          "thumbnailMimeType": {},
          "type": 1,
          "updatedAt": "string"
        }
      ],
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachableId` | object |  |
| `attachableType` | object |  |
| `companyId` | number |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `isDemo` | boolean |  |
| `isHidden` | boolean |  |
| `isLocked` | boolean |  |
| `isShared` | boolean |  |
| `name` | string |  |
| `nodes[].attachableId` | object |  |
| `nodes[].attachableType` | object |  |
| `nodes[].companyId` | number |  |
| `nodes[].createdAt` | string |  |
| `nodes[].deletedAt` | object |  |
| `nodes[].id` | number |  |
| `nodes[].isDefault` | number |  |
| `nodes[].isDemo` | number |  |
| `nodes[].isHidden` | number |  |
| `nodes[].isLocked` | number |  |
| `nodes[].isShared` | number |  |
| `nodes[].mediaFileIdAsParentDirectory` | object |  |
| `nodes[].name` | string |  |
| `nodes[].nodes[].attachableId` | object |  |
| `nodes[].nodes[].attachableType` | object |  |
| `nodes[].nodes[].companyId` | number |  |
| `nodes[].nodes[].createdAt` | string |  |
| `nodes[].nodes[].deletedAt` | object |  |
| `nodes[].nodes[].id` | number |  |
| `nodes[].nodes[].isDefault` | number |  |
| `nodes[].nodes[].isDemo` | number |  |
| `nodes[].nodes[].isHidden` | number |  |
| `nodes[].nodes[].isLocked` | number |  |
| `nodes[].nodes[].isShared` | number |  |
| `nodes[].nodes[].mediaFileIdAsParentDirectory` | number |  |
| `nodes[].nodes[].name` | string |  |
| `nodes[].nodes[].status` | object |  |
| `nodes[].nodes[].thumbnailExtension` | object |  |
| `nodes[].nodes[].thumbnailHash` | object |  |
| `nodes[].nodes[].thumbnailMimeType` | object |  |
| `nodes[].nodes[].type` | number |  |
| `nodes[].nodes[].updatedAt` | string |  |
| `nodes[].status` | object |  |
| `nodes[].thumbnailExtension` | object |  |
| `nodes[].thumbnailHash` | object |  |
| `nodes[].thumbnailMimeType` | object |  |
| `nodes[].type` | number |  |
| `nodes[].updatedAt` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Viewneo API, this operation is `GET /treeview` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-tree.md) for the provider-specific parameters and requirements.

