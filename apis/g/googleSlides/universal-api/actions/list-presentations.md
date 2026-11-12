# Google Slides: List Presentations

Lists the Google Slides presentations the connection can access, excluding trashed files.

```
GET https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/list-presentations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/list-presentations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/list-presentations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Comma-separated sort keys: createdTime, folder, modifiedByMeTime, modifiedTime, name, name_natural, quotaBytesUsed, recency, sharedWithMeTime, starred, viewedByMeTime. Append desc to reverse a key. Example: `modifiedTime desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "starred": true,
      "webViewLink": "https://example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | The presentation title. |
| `modifiedTime` | date | When the presentation was last modified. |
| `createdTime` | date | When the presentation was created. |
| `starred` | boolean | Whether the user starred the presentation. |
| `webViewLink` | string | Link to open the presentation in Google Slides. |
| `id` | string | The presentation ID. |

## Native endpoint

Through the native Google Slides API, this operation is `GET /drive/v3/files` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-presentations.md) for the provider-specific parameters and requirements.

