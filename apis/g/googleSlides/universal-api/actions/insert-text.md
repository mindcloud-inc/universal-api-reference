# Google Slides: Insert Text

Inserts text into a shape, text box, placeholder, or table cell on a slide.

```
PUT https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/insert-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/insert-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "objectId": "i0",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/insert-text', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "objectId": "i0",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `objectId` | string | yes | Object ID of the shape or table to insert text into. Example: `i0`. |
| `text` | string | yes | Text to insert. A newline starts a new paragraph. |
| `insertionIndex` | number | no | Zero-based index, in Unicode code units, where the text is inserted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cellLocation` | object | no | Only for table cells; Object ID must then be a table. |
| `cellLocation.rowIndex` | number | no | Zero-based row index. |
| `cellLocation.columnIndex` | number | no | Zero-based column index. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "presentationId": "string",
      "writeControl": {
        "requiredRevisionId": "string"
      },
      "commentUpdateState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `presentationId` | string | The ID of the presentation that was updated. |
| `writeControl.requiredRevisionId` | string | Revision ID of the presentation after the update, usable for conditional writes. |
| `commentUpdateState` | string | Whether the request changed comments. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-text.md) for the provider-specific parameters and requirements.

