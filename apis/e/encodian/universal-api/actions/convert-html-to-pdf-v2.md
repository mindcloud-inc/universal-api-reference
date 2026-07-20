# Encodian: Convert HTML To PDF V2

Converts HTML to PDF in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-html-to-pdf-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-html-to-pdf-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-html-to-pdf-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `htmlData` | string | no | Example: `<html><body><h1>Hello Encodian</h1></body></html>`. |
| `htmlUrl` | string | no | Example: `https://example.com`. |
| `filename` | string | no | Example: `sample.html`. |
| `fileContent` | string | no | Example: `Base64 encoded HTML file content`. |
| `pageOrientation` | string | no | Example: `Portrait`. |
| `pageSize` | string | no | Example: `A4`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createBookmarks` | boolean | no |  |
| `createTableOfContents` | boolean | no |  |
| `cssType` | string | no | Example: `Print`. |
| `decodeHtmlData` | boolean | no |  |
| `delay` | number | no | Example: `1000`. |
| `enableHyperlinks` | boolean | no |  |
| `enableJavaScript` | boolean | no |  |
| `topMargin` | number | no | Default: `0`. Example: `0`. |
| `bottomMargin` | number | no | Default: `0`. Example: `0`. |
| `rightMargin` | number | no | Default: `0`. Example: `0`. |
| `leftMargin` | number | no | Default: `0`. Example: `0`. |
| `pageRotation` | string | no | Example: `0`. |
| `scale` | number | no | Example: `1`. |
| `viewPort` | string | no | Example: `1280x720`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "fileContent": "string",
      "filename": "Ava Chen",
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Errors returned by Encodian, if any. |
| `fileContent` | string | The Base64 encoded generated PDF when available. |
| `filename` | string | The generated PDF file name when available. |
| `httpStatusCode` | number | The HTTP status code returned by Encodian. |
| `httpStatusMessage` | string | The HTTP status message returned by Encodian. |
| `operationId` | string | The Encodian operation ID for the queued conversion. |
| `operationStatus` | string | The Encodian operation status. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Conversion/HtmlToPDFV2` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-html-to-pdf-v2.md) for the provider-specific parameters and requirements.

