# Encodian: PowerPoint Merge Files

Merges PowerPoint files in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-merge-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-merge-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mergePresentationOutputFormat": "string",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-merge-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mergePresentationOutputFormat": "string",
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mergePresentationOutputFormat` | string | yes | The output presentation format, such as PPTX. |
| `outputFilename` | string | no | Optional filename for the merged presentation; defaults to presentation. |
| `documents[]` | array<object> | yes | Array of presentations to merge. Each item includes fileName, fileContent, optional sortPosition, and optional slidesToMerge. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mergePresentationMasterStyle` | boolean | no | Apply the first presentation style to all other presentations. |

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
| `Errors` | array<string> | Errors returned by Encodian, if any. |
| `FileContent` | string | The Base64 encoded merged presentation file. |
| `Filename` | string | The filename of the merged presentation. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PowerPoint/MergePresentations` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/power-point-merge-files.md) for the provider-specific parameters and requirements.

