# Google Slides: Batch Update Presentation

Applies one or more batch update requests to a presentation in a single atomic call. Use the dedicated actions for common single changes.

```
PUT https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/batch-update-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/batch-update-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "requests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/batch-update-presentation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "requests[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `requests[]` | array<object> | yes | Batch update requests, each an object with one request type (for example createSlide, insertText, replaceAllText). The Request union has 49 request types, so items are passed as raw JSON. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `writeControl` | object | no | Optional conditional-write settings. |
| `writeControl.requiredRevisionId` | string | no | Only apply the update when this is still the latest revision of the presentation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replies": [
        {}
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
| `replies` | array<object> | One reply per request, in request order. Each reply holds the result for its request type, or is empty. |
| `presentationId` | string | The ID of the presentation that was updated. |
| `writeControl.requiredRevisionId` | string | Revision ID of the presentation after the update, usable for conditional writes. |
| `commentUpdateState` | string | Whether the request changed comments. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-presentation.md) for the provider-specific parameters and requirements.

