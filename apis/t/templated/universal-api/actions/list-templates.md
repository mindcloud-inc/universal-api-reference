# Templated: List Templates

Retrieves all template records from Templated.

```
GET https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-templates?${params}`, {
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
| `query` | string | no | Filter templates by name. |
| `width` | number | no | Filter templates by width. |
| `height` | number | no | Filter templates by height. |
| `tags` | string | no | Filter templates by comma-separated tags. |
| `externalId` | string | no | Filter templates by external ID. |
| `includeLayers` | boolean | no | Include template layers in the response. |
| `includePages` | boolean | no | Include template pages and layers in the response. |

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

Through the native Templated API, this operation is `GET /v1/templates` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

