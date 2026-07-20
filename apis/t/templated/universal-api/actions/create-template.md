# Templated: Create Template

Creates a new template in Templated.

```
POST https://connect.mindcloud.co/v1/universal/templated/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/templated/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "width": 1,
  "height": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/templated/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "width": 1,
    "height": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the template. |
| `width` | number | yes | The width of the template in pixels. |
| `height` | number | yes | The height of the template in pixels. |
| `layers[]` | array<object> | no | Single-page layer definitions for the template. |
| `pages[]` | array<object> | no | Multi-page definitions for the template. |
| `duration` | number | no | Default video duration in milliseconds for MP4 renders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "categoryName": "Ava Chen",
      "createdAt": "string",
      "description": "string",
      "duration": 1,
      "externalId": "string",
      "folderId": "string",
      "folderName": "Ava Chen",
      "height": 1,
      "html": "string",
      "id": "string",
      "isClone": true,
      "isMaster": true,
      "layersCount": 1,
      "multiSizePages": true,
      "name": "Ava Chen",
      "pagesCount": 1,
      "ranking": 1,
      "removed": true,
      "sourceTemplateId": "string",
      "sourceTemplateName": "Ava Chen",
      "tags": [
        "string"
      ],
      "teamId": "string",
      "thumbnail": "string",
      "type": "string",
      "updatedAt": "string",
      "userId": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string |  |
| `categoryName` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `externalId` | string |  |
| `folderId` | string |  |
| `folderName` | string |  |
| `height` | number |  |
| `html` | string |  |
| `id` | string |  |
| `isClone` | boolean |  |
| `isMaster` | boolean |  |
| `layersCount` | number |  |
| `multiSizePages` | boolean |  |
| `name` | string |  |
| `pagesCount` | number |  |
| `ranking` | number |  |
| `removed` | boolean |  |
| `sourceTemplateId` | string |  |
| `sourceTemplateName` | string |  |
| `tags` | array<string> |  |
| `teamId` | string |  |
| `thumbnail` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Templated API, this operation is `POST /v1/template` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

