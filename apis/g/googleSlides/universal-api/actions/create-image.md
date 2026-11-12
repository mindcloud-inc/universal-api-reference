# Google Slides: Create Image

Inserts an image from a public URL onto a slide.

```
POST https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "url": "https://example.com/chart.png",
  "elementProperties.pageObjectId": "p"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "url": "https://example.com/chart.png",
    "elementProperties.pageObjectId": "p"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `url` | string | yes | Public PNG, JPEG or GIF URL, at most 2 KB long. The image must be under 50 MB and 25 megapixels. Example: `https://example.com/chart.png`. |
| `elementProperties` | object | no |  |
| `elementProperties.pageObjectId` | string | yes | The object ID of the slide the element is placed on. Example: `p`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `elementProperties.size` | object | no |  |
| `elementProperties.size.width` | object | no |  |
| `elementProperties.size.width.magnitude` | number | no |  |
| `elementProperties.size.width.unit` | list<string> | no | One of: `EMU`, `PT`, `UNIT_UNSPECIFIED`. |
| `elementProperties.size.height` | object | no |  |
| `elementProperties.size.height.magnitude` | number | no |  |
| `elementProperties.size.height.unit` | list<string> | no | One of: `EMU`, `PT`, `UNIT_UNSPECIFIED`. |
| `elementProperties.transform` | object | no |  |
| `elementProperties.transform.scaleX` | number | no |  |
| `elementProperties.transform.scaleY` | number | no |  |
| `elementProperties.transform.shearX` | number | no |  |
| `elementProperties.transform.shearY` | number | no |  |
| `elementProperties.transform.translateX` | number | no |  |
| `elementProperties.transform.translateY` | number | no |  |
| `elementProperties.transform.unit` | list<string> | no | Units for the translate elements. One of: `EMU`, `PT`, `UNIT_UNSPECIFIED`. |
| `objectId` | string | no | Optional custom ID for the new object: 5-50 characters, starting with a letter, digit or underscore. Generated when omitted. Example: `myObject_01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replies": [
        {
          "createImage": {
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
| `replies[].createImage.objectId` | string | Object ID of the new image. |
| `presentationId` | string | The ID of the presentation that was updated. |
| `writeControl.requiredRevisionId` | string | Revision ID of the presentation after the update, usable for conditional writes. |
| `commentUpdateState` | string | Whether the request changed comments. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

