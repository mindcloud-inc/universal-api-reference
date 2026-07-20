# Instructure: Get Page

Retrieves a page from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-page?connectionId=$CONNECTION_ID&courseId=1&pageId=mindcloud-validation-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "1",
  "pageId": "mindcloud-validation-page"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-page?${params}`, {
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
| `pageId` | string | yes | The Canvas page identifier. Default: `mindcloud-validation-page`. |

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

Through the native Instructure API, this operation is `GET /courses/:course_id/pages/:page_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

