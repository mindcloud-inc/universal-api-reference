# Google Slides: Delete Text

Deletes all or part of the text in a shape, text box, placeholder, or table cell.

```
PUT https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/delete-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/delete-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "objectId": "i0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/delete-text', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "objectId": "i0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `objectId` | string | yes | Object ID of the shape or table to delete text from. Example: `i0`. |
| `textRange` | object | no |  |
| `textRange.type` | list<string> | no | Fixed Range needs start and end index, From Start Index needs only start index, All needs neither. One of: `ALL`, `FIXED_RANGE`, `FROM_START_INDEX`, `RANGE_TYPE_UNSPECIFIED`. |
| `textRange.startIndex` | number | no | Zero-based start of the range. |
| `textRange.endIndex` | number | no | Zero-based exclusive end of the range. Only for Fixed Range. |

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

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-text.md) for the provider-specific parameters and requirements.

