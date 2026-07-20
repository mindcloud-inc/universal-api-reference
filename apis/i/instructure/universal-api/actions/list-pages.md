# Instructure: List Pages

Retrieves pages from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&courseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "courseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-pages?${params}`, {
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
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "editingRoles": "string",
      "hideFromStudents": true,
      "htmlUrl": "https://example.com",
      "pageId": "string",
      "published": true,
      "title": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `editingRoles` | string |  |
| `hideFromStudents` | boolean |  |
| `htmlUrl` | string |  |
| `pageId` | string |  |
| `published` | boolean |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /courses/:course_id/pages` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

