# Document360: Create Article



```
POST https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "projectVersionId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "projectVersionId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The title of the article |
| `content` | string | no | The article content |
| `categoryId` | string | no | The category where the article will be created |
| `projectVersionId` | string | yes | The project version where the article will be created |
| `userId` | string | yes | The team account that will be marked as contributor |
| `order` | number | no | The position inside the category |
| `contentType` | number | no | The editor type |
| `slug` | string | no | Optional custom slug |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": 1,
      "currentWorkflowStatusId": "string",
      "hidden": true,
      "id": "string",
      "isSharedArticle": true,
      "languageCode": "string",
      "latestVersion": 1,
      "modifiedAt": "string",
      "order": 1,
      "publicVersion": 1,
      "slug": "string",
      "status": 1,
      "title": "string",
      "translationOption": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | number |  |
| `currentWorkflowStatusId` | string |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `isSharedArticle` | boolean |  |
| `languageCode` | string |  |
| `latestVersion` | number |  |
| `modifiedAt` | string |  |
| `order` | number |  |
| `publicVersion` | number |  |
| `slug` | string |  |
| `status` | number |  |
| `title` | string |  |
| `translationOption` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `POST /v2/Articles` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-article.md) for the provider-specific parameters and requirements.

