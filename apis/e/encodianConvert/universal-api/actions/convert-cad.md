# Encodian - Convert: Convert - CAD

Creates a converted file from a CAD file in Encodian - Convert.

```
POST https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-cad
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-cad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFormatParameter": "string",
  "outputFilename": "Ava Chen",
  "fileName": "Ava Chen",
  "fileContent": "string",
  "outputFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-cad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFormatParameter": "string",
    "outputFilename": "Ava Chen",
    "fileName": "Ava Chen",
    "fileContent": "string",
    "outputFormat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFormatParameter` | string | yes | Set the output file type used by Encodian's dynamic schema. |
| `outputFilename` | string | yes | The filename of the output document. |
| `fileName` | string | yes | The filename of the source file, including extension. |
| `fileContent` | file | yes | The file content of the source CAD file. |
| `outputFormat` | string | yes | The format of the output file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Errors returned by Encodian. |
| `FileContent` | string | Processed document content, usually Base64 encoded. |
| `Filename` | string | Filename of the processed document. |
| `HttpStatusCode` | number | HTTP status code returned by Encodian. |
| `HttpStatusMessage` | string | HTTP status message returned by Encodian. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Convert API, this operation is `POST /api/v1/Conversion/ConvertCad` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-cad.md) for the provider-specific parameters and requirements.

