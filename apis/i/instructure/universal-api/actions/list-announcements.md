# Instructure: List Announcements

Retrieves announcements from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-announcements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-announcements?connectionId=$CONNECTION_ID&limit=25&offset=0&contextCodes=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contextCodes": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/list-announcements?${params}`, {
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
| `contextCodes` | string | yes | One or more Canvas context codes such as course_123. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discussionType": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "lastReplyAt": "string",
      "message": "string",
      "postedAt": "string",
      "published": true,
      "requireInitialPost": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discussionType` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `lastReplyAt` | string |  |
| `message` | string |  |
| `postedAt` | string |  |
| `published` | boolean |  |
| `requireInitialPost` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /announcements` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-announcements.md) for the provider-specific parameters and requirements.

