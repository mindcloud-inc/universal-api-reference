# Google Slides: Update Slides Position

Moves one or more slides to a new position in the presentation.

```
PUT https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/update-slides-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/update-slides-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "slideObjectIds[]": [
    "string"
  ],
  "insertionIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/update-slides-position', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "slideObjectIds[]": ["string"],
    "insertionIndex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `slideObjectIds[]` | array<string> | yes | IDs of the slides to move, in their current presentation order, without duplicates. |
| `insertionIndex` | number | yes | Zero-based position to move the slides to, based on the order before the move. Must be between 0 and the slide count. |

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

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-slides-position.md) for the provider-specific parameters and requirements.

