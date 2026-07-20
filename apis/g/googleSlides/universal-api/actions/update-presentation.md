# Google Slides: Update Presentation

Updates an existing presentation file in Google Slides.

```
PUT https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/update-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/update-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/update-presentation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | The ID of the presentation file to update. |
| `name` | string | yes | The new file name for the presentation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "kind": "string",
      "mimeType": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The file ID of the presentation. |
| `kind` | string | The Drive resource type. |
| `mimeType` | string | The file MIME type. |
| `name` | string | The updated file name. |

## Native endpoint

Through the native Google Slides API, this operation is `PATCH https://www.googleapis.com/drive/v3/files/:fileId` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-presentation.md) for the provider-specific parameters and requirements.

