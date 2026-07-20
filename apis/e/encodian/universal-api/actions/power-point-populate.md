# Encodian: PowerPoint Populate

Populates a PowerPoint file in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-populate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-populate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string",
  "jsonData": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-populate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string",
    "jsonData": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | A Base64 encoded representation of the PowerPoint file to be processed |
| `jsonData` | string | yes | A JSON string containing the data used to populate template tokens Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jsonParseMode` | string | no | Set how JSON data should be parsed Default: `Standard`. |
| `allowMissingMembers` | boolean | no | Set whether missing token values should be ignored |
| `inlineErrorMessages` | boolean | no | Set whether token errors should be written inline in the document |
| `removeEmptyParagraphs` | boolean | no | Set whether empty paragraphs should be removed |
| `dateTimeFormat` | string | no | Optional JSON mapping for custom date and time formats |
| `multipleSlides` | boolean | no | Set whether array data should duplicate slides for repeated items |
| `cultureName` | string | no | Set the culture used when processing values |

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
| `FileContent` | string | The Base64 encoded populated presentation file. |
| `Filename` | string | The filename of the populated presentation. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PowerPoint/PopulatePowerPoint` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/power-point-populate.md) for the provider-specific parameters and requirements.

