# Base64.ai: OCR Document by URL

Creates an OCR result in Base64.ai from a document URL.

```
POST https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/ocr-document-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/ocr-document-by-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/ocr-document-by-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the document to OCR. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": {
        "creditsSpent": 1,
        "dom": {
          "box": {
            "bottom": 1,
            "height": 1,
            "left": 1,
            "pageNumber": {},
            "right": 1,
            "top": 1,
            "width": 1
          },
          "confidence": 1,
          "pages": [
            {
              "box": {
                "bottom": 1,
                "height": 1,
                "left": 1,
                "pageNumber": 1,
                "right": 1,
                "top": 1,
                "width": 1
              },
              "confidence": 1,
              "location": {
                "bottomLeft": {
                  "x": 1,
                  "y": 1
                },
                "bottomRight": {
                  "x": 1,
                  "y": 1
                },
                "pageNumber": 1,
                "topLeft": {
                  "x": 1,
                  "y": 1
                },
                "topRight": {
                  "x": 1,
                  "y": 1
                }
              },
              "properties": {
                "dpiX": 1,
                "dpiY": 1,
                "height": 1,
                "mimeType": "string",
                "normalizedHeight": 1,
                "normalizedWidth": 1,
                "rotationAngle": 1,
                "width": 1
              },
              "text": "string"
            }
          ],
          "text": "string"
        },
        "fraud": {
          "indicators": [
            {
              "category": "string",
              "confidence": "string",
              "description": "string",
              "evidences": [
                {
                  "ocr": "string"
                }
              ],
              "name": "Ava Chen",
              "risk": "string"
            }
          ],
          "risk": "string"
        },
        "properties": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "documentPageCount": 1,
          "dpiX": 1,
          "dpiY": 1,
          "flowID": "string",
          "height": 1,
          "isEditable": true,
          "isFirstPageOfResult": true,
          "isGlareFree": true,
          "isInFocus": true,
          "isSelectable": true,
          "mimeType": "string",
          "originalFileName": "Ava Chen",
          "pageCount": 1,
          "rotationAngle": 1,
          "startPage": 1,
          "width": 1
        }
      },
      "fields": {},
      "model": {
        "confidence": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "ocr": "string",
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features.creditsSpent` | number |  |
| `features.dom.box.bottom` | number |  |
| `features.dom.box.height` | number |  |
| `features.dom.box.left` | number |  |
| `features.dom.box.pageNumber` | object |  |
| `features.dom.box.right` | number |  |
| `features.dom.box.top` | number |  |
| `features.dom.box.width` | number |  |
| `features.dom.confidence` | number |  |
| `features.dom.pages[].box.bottom` | number |  |
| `features.dom.pages[].box.height` | number |  |
| `features.dom.pages[].box.left` | number |  |
| `features.dom.pages[].box.pageNumber` | number |  |
| `features.dom.pages[].box.right` | number |  |
| `features.dom.pages[].box.top` | number |  |
| `features.dom.pages[].box.width` | number |  |
| `features.dom.pages[].confidence` | number |  |
| `features.dom.pages[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].location.bottomRight.x` | number |  |
| `features.dom.pages[].location.bottomRight.y` | number |  |
| `features.dom.pages[].location.pageNumber` | number |  |
| `features.dom.pages[].location.topLeft.x` | number |  |
| `features.dom.pages[].location.topLeft.y` | number |  |
| `features.dom.pages[].location.topRight.x` | number |  |
| `features.dom.pages[].location.topRight.y` | number |  |
| `features.dom.pages[].properties.dpiX` | number |  |
| `features.dom.pages[].properties.dpiY` | number |  |
| `features.dom.pages[].properties.height` | number |  |
| `features.dom.pages[].properties.mimeType` | string |  |
| `features.dom.pages[].properties.normalizedHeight` | number |  |
| `features.dom.pages[].properties.normalizedWidth` | number |  |
| `features.dom.pages[].properties.rotationAngle` | number |  |
| `features.dom.pages[].properties.width` | number |  |
| `features.dom.pages[].text` | string |  |
| `features.dom.text` | string |  |
| `features.fraud.indicators[].category` | string |  |
| `features.fraud.indicators[].confidence` | string |  |
| `features.fraud.indicators[].description` | string |  |
| `features.fraud.indicators[].evidences[].ocr` | string |  |
| `features.fraud.indicators[].name` | string |  |
| `features.fraud.indicators[].risk` | string |  |
| `features.fraud.risk` | string |  |
| `features.properties.createdAt` | date |  |
| `features.properties.documentPageCount` | number |  |
| `features.properties.dpiX` | number |  |
| `features.properties.dpiY` | number |  |
| `features.properties.flowID` | string |  |
| `features.properties.height` | number |  |
| `features.properties.isEditable` | boolean |  |
| `features.properties.isFirstPageOfResult` | boolean |  |
| `features.properties.isGlareFree` | boolean |  |
| `features.properties.isInFocus` | boolean |  |
| `features.properties.isSelectable` | boolean |  |
| `features.properties.mimeType` | string |  |
| `features.properties.originalFileName` | string |  |
| `features.properties.pageCount` | number |  |
| `features.properties.rotationAngle` | number |  |
| `features.properties.startPage` | number |  |
| `features.properties.width` | number |  |
| `fields` | object |  |
| `model.confidence` | number |  |
| `model.name` | string |  |
| `model.type` | string |  |
| `ocr` | string |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `POST /api/scan` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ocr-document-by-url.md) for the provider-specific parameters and requirements.

