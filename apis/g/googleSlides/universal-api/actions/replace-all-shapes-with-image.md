# Google Slides: Replace All Shapes with Image

Replaces every shape that contains a given text with an image, useful for filling image placeholders in templates.

```
PUT https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/replace-all-shapes-with-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/replace-all-shapes-with-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "containsText.text": "{{customer_name}}",
  "imageUrl": "https://example.com/logo.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/replace-all-shapes-with-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "containsText.text": "{{customer_name}}",
    "imageUrl": "https://example.com/logo.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `containsText` | object | no |  |
| `containsText.text` | string | yes | The text to search for in shapes and tables. Example: `{{customer_name}}`. |
| `containsText.matchCase` | boolean | no | Whether the search is case sensitive. |
| `imageUrl` | string | yes | Public PNG, JPEG or GIF URL, at most 2 KB long. The image must be under 50 MB and 25 megapixels. Example: `https://example.com/logo.png`. |
| `imageReplaceMethod` | list<string> | no | Center Inside fits the image inside the shape keeping its aspect ratio; Center Crop fills the shape and may crop the image. One of: `CENTER_CROP`, `CENTER_INSIDE`, `IMAGE_REPLACE_METHOD_UNSPECIFIED`. Default: `CENTER_INSIDE`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `containsText.searchByRegex` | boolean | no | Treat the search text as a regular expression; backslashes must be escaped. |
| `pageObjectIds[]` | array<string> | no | Limit the change to these slide IDs. Applies to all slides when empty. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replies": [
        {
          "replaceAllShapesWithImage": {
            "occurrencesChanged": 1
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
| `replies[].replaceAllShapesWithImage.occurrencesChanged` | number | Number of shapes replaced with the image. |
| `presentationId` | string | The ID of the presentation that was updated. |
| `writeControl.requiredRevisionId` | string | Revision ID of the presentation after the update, usable for conditional writes. |
| `commentUpdateState` | string | Whether the request changed comments. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-all-shapes-with-image.md) for the provider-specific parameters and requirements.

