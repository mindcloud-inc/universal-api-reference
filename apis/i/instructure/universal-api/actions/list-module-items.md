# Instructure: List Module Items

Retrieves module items from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-module-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-module-items?connectionId=$CONNECTION_ID&limit=25&offset=0&courseId=1&moduleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "courseId": "1",
  "moduleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-module-items?${params}`, {
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
| `moduleId` | string | yes | The Canvas module ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentId": 1,
      "htmlUrl": "https://example.com",
      "id": 1,
      "moduleId": 1,
      "position": 1,
      "published": true,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentId` | number |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `moduleId` | number |  |
| `position` | number |  |
| `published` | boolean |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /courses/:course_id/modules/:module_id/items` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-module-items.md) for the provider-specific parameters and requirements.

