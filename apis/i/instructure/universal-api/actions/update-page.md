# Instructure: Update Page

Updates an existing page in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "1",
  "pageId": "mindcloud-validation-page"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "1",
    "pageId": "mindcloud-validation-page"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `pageId` | string | yes | The Canvas page identifier. Default: `mindcloud-validation-page`. |
| `title` | string | no | Page title. |
| `body` | string | no | Page body HTML or text. |

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

Through the native Instructure API, this operation is `PUT /courses/:course_id/pages/:page_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

