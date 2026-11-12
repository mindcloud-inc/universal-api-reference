# Google Slides: Create Slide

Adds a new slide to a presentation, optionally at a position and with a predefined or existing layout.

```
POST https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-slide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-slide" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-slide', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `insertionIndex` | number | no | Zero-based position for the new slide. Appends to the end when omitted. |
| `slideLayoutReference` | object | no |  |
| `slideLayoutReference.predefinedLayout` | list<string> | no | Predefined layout from the current master. Not every master contains every layout. One of: `BIG_NUMBER`, `BLANK`, `CAPTION_ONLY`, `MAIN_POINT`, `ONE_COLUMN_TEXT`, `PREDEFINED_LAYOUT_UNSPECIFIED`, `SECTION_HEADER`, `SECTION_TITLE_AND_DESCRIPTION`, `TITLE`, `TITLE_AND_BODY`, `TITLE_AND_TWO_COLUMNS`, `TITLE_ONLY`. Default: `BLANK`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slideLayoutReference.layoutId` | string | no | Object ID of a layout in the presentation. Use instead of Predefined Layout. |
| `objectId` | string | no | Optional custom ID for the new object: 5-50 characters, starting with a letter, digit or underscore. Generated when omitted. Example: `myObject_01`. |
| `placeholderIdMappings[]` | array<object> | no | Assign your own object IDs to layout placeholders created on the slide, so later actions can target them. |
| `placeholderIdMappings[].objectId` | string | no | Custom ID for the placeholder created on the slide. |
| `placeholderIdMappings[].layoutPlaceholder` | object | no |  |
| `placeholderIdMappings[].layoutPlaceholder.type` | list<string> | no | One of: `BODY`, `CENTERED_TITLE`, `CHART`, `CLIP_ART`, `DATE_AND_TIME`, `DIAGRAM`, `FOOTER`, `HEADER`, `MEDIA`, `NONE`, `OBJECT`, `PICTURE`, `SLIDE_IMAGE`, `SLIDE_NUMBER`, `SUBTITLE`, `TABLE`, `TITLE`. |
| `placeholderIdMappings[].layoutPlaceholder.index` | number | no |  |
| `placeholderIdMappings[].layoutPlaceholderObjectId` | string | no | Object ID of the layout placeholder. Use instead of Layout Placeholder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replies": [
        {
          "createSlide": {
            "objectId": "string"
          }
        }
      ],
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
| `replies[].createSlide.objectId` | string | Object ID of the new slide. |
| `presentationId` | string | The ID of the presentation that was updated. |
| `writeControl.requiredRevisionId` | string | Revision ID of the presentation after the update, usable for conditional writes. |
| `commentUpdateState` | string | Whether the request changed comments. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-slide.md) for the provider-specific parameters and requirements.

