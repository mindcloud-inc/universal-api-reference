# Bannerbite: Get Bite

Retrieves a bite from Bannerbite by ID.

```
GET https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/get-bite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/get-bite?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/get-bite?${params}`, {
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
| `id` | number | yes | The Bannerbite bite ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accessToken": "string",
        "biteSizeId": 1,
        "content": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "generatedLottie": {},
        "id": 1,
        "name": "Ava Chen",
        "output": {},
        "projectId": 1,
        "settings": "string",
        "size": {
          "backgroundColor": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "height": 1,
          "icon": {},
          "id": 1,
          "name": "Ava Chen",
          "slug": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userId": {},
          "width": 1
        },
        "slug": "string",
        "template": {
          "audioPath": {},
          "categories": "string",
          "categoryId": {},
          "content": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": {},
          "externalId": {},
          "filePath": "string",
          "id": 1,
          "isAllowVideo": 1,
          "isDefault": 1,
          "isPublished": 1,
          "name": "Ava Chen",
          "size": "string",
          "slug": "string",
          "thumbnailLargePath": {},
          "thumbnailPath": "string",
          "type": {},
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "uploadFrom": "string",
          "userId": 1,
          "videoPreviewLarge": {},
          "videoPreviewSmall": "string"
        },
        "templateId": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accessToken` | string |  |
| `data.biteSizeId` | number |  |
| `data.content` | string |  |
| `data.createdAt` | date |  |
| `data.generatedLottie` | object |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.output` | object |  |
| `data.projectId` | number |  |
| `data.settings` | string |  |
| `data.size.backgroundColor` | string |  |
| `data.size.createdAt` | date |  |
| `data.size.description` | string |  |
| `data.size.height` | number |  |
| `data.size.icon` | object |  |
| `data.size.id` | number |  |
| `data.size.name` | string |  |
| `data.size.slug` | string |  |
| `data.size.updatedAt` | date |  |
| `data.size.userId` | object |  |
| `data.size.width` | number |  |
| `data.slug` | string |  |
| `data.template.audioPath` | object |  |
| `data.template.categories` | string |  |
| `data.template.categoryId` | object |  |
| `data.template.content` | string |  |
| `data.template.createdAt` | date |  |
| `data.template.description` | object |  |
| `data.template.externalId` | object |  |
| `data.template.filePath` | string |  |
| `data.template.id` | number |  |
| `data.template.isAllowVideo` | number |  |
| `data.template.isDefault` | number |  |
| `data.template.isPublished` | number |  |
| `data.template.name` | string |  |
| `data.template.size` | string |  |
| `data.template.slug` | string |  |
| `data.template.thumbnailLargePath` | object |  |
| `data.template.thumbnailPath` | string |  |
| `data.template.type` | object |  |
| `data.template.updatedAt` | date |  |
| `data.template.uploadFrom` | string |  |
| `data.template.userId` | number |  |
| `data.template.videoPreviewLarge` | object |  |
| `data.template.videoPreviewSmall` | string |  |
| `data.templateId` | number |  |
| `data.updatedAt` | date |  |
| `data.userId` | number |  |

## Native endpoint

Through the native Bannerbite API, this operation is `GET /api/bites/:id` (base URL `https://api.bannerbite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bite.md) for the provider-specific parameters and requirements.

