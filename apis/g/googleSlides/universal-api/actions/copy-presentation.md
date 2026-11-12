# Google Slides: Copy Presentation

Creates a copy of an existing presentation, optionally with a new title.

```
POST https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/copy-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/copy-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/copy-presentation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | list<string> | yes | The ID of the presentation to copy. |
| `name` | string | no | Title for the new copy. Google names it "Copy of" the original title when omitted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "createdTime": "2026-05-07T12:00:00.000Z",
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
| `webViewLink` | string | Link to open the presentation in Google Slides. |
| `id` | string | The presentation ID. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /drive/v3/files/:fileId/copy` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-presentation.md) for the provider-specific parameters and requirements.

