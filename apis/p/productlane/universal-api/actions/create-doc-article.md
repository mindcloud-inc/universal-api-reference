# Productlane: Create Doc Article

Creates a help center article in Productlane.

```
POST https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-doc-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-doc-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Stage 3 Test Article",
  "content": "# Stage 3 test article",
  "groupId": "a48ae618-61e4-4ec1-b23a-56ac476c95d5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-doc-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Stage 3 Test Article",
    "content": "# Stage 3 test article",
    "groupId": "a48ae618-61e4-4ec1-b23a-56ac476c95d5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Doc article title. Example: `Stage 3 Test Article`. |
| `content` | string | yes | Markdown content for the doc article. Example: `# Stage 3 test article`. |
| `groupId` | string | yes | Target docs group ID. Example: `a48ae618-61e4-4ec1-b23a-56ac476c95d5`. |
| `summary` | string | no | Article summary. Example: `Short summary`. |
| `published` | boolean | no | Whether the article should be published immediately. Default: `true`. |
| `language` | string | no | Language code for the article. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "helpCenterGroupId": "string",
      "icon": "string",
      "id": "string",
      "imageBlurhash": "string",
      "imageUrl": "https://example.com",
      "isDeleted": true,
      "order": 1,
      "published": true,
      "showOnHomePage": true,
      "summary": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urlName": "https://example.com",
      "version": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `content` | string |  |
| `createdAt` | date |  |
| `date` | date |  |
| `helpCenterGroupId` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `imageBlurhash` | string |  |
| `imageUrl` | string |  |
| `isDeleted` | boolean |  |
| `order` | number |  |
| `published` | boolean |  |
| `showOnHomePage` | boolean |  |
| `summary` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `urlName` | string |  |
| `version` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Productlane API, this operation is `POST /docs/articles` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-doc-article.md) for the provider-specific parameters and requirements.

