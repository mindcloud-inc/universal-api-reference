# Document360: Get Category



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-category?connectionId=$CONNECTION_ID&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-category?${params}`, {
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
| `categoryId` | string | yes |  |
| `langCode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": [
        {}
      ],
      "categoryType": 1,
      "childCategories": [
        {}
      ],
      "contentType": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentWorkflowStatusId": "string",
      "description": "string",
      "hidden": true,
      "icon": "string",
      "id": "string",
      "languageCode": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "order": 1,
      "parentCategoryId": "string",
      "projectVersionId": "string",
      "slug": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> |  |
| `categoryType` | number |  |
| `childCategories` | array<object> |  |
| `contentType` | number |  |
| `createdAt` | date |  |
| `currentWorkflowStatusId` | string |  |
| `description` | string |  |
| `hidden` | boolean |  |
| `icon` | string |  |
| `id` | string |  |
| `languageCode` | string |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `order` | number |  |
| `parentCategoryId` | string |  |
| `projectVersionId` | string |  |
| `slug` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Categories/:categoryId` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category.md) for the provider-specific parameters and requirements.

