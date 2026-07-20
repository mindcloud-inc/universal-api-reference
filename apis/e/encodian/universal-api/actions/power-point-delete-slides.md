# Encodian: PowerPoint Delete Slides

Deletes PowerPoint slides in Encodian.

```
DELETE https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-delete-slides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-delete-slides?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-delete-slides?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | The Base64 encoded content of the Microsoft PowerPoint file. |
| `slideNumbers` | string | no | Comma-separated slide indexes to delete, such as 1,3,4. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startSlide` | number | no | Slide index where deletion starts. |
| `endSlide` | number | no | Slide index where deletion stops; defaults to the last slide. |
| `cultureName` | string | no | Culture name used when processing the request. |

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
| `FileContent` | string | The Base64 encoded processed presentation file. |
| `Filename` | string | The filename of the processed file. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PowerPoint/PowerPointDeleteSlides` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/power-point-delete-slides.md) for the provider-specific parameters and requirements.

