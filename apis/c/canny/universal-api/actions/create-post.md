# Canny: Create Post

Creates a new post in Canny.

```
POST https://connect.mindcloud.co/v1/universal/canny/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/canny/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authorID": "string",
  "boardID": "string",
  "title": "string",
  "details": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canny/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authorID": "string",
    "boardID": "string",
    "title": "string",
    "details": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorID` | string | yes |  |
| `boardID` | string | yes |  |
| `title` | string | yes |  |
| `details` | string | yes |  |
| `categoryID` | string | no |  |
| `ownerID` | string | no |  |
| `byID` | string | no |  |
| `eta` | string | no |  |
| `etaPublic` | boolean | no |  |
| `imageURLs` | list<string> | no |  |
| `customFields` | object | no |  |
| `createdAt` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v1/posts/create` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

