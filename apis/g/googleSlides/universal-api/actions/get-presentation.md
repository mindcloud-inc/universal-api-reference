# Google Slides: Get Presentation

Retrieves a presentation from Google Slides.

```
GET https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-presentation?connectionId=$CONNECTION_ID&presentationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-presentation?${params}`, {
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
| `presentationId` | string | yes | The ID of the presentation to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "layouts": [
        {}
      ],
      "locale": "string",
      "masters": [
        {}
      ],
      "pageSize": {},
      "presentationId": "string",
      "revisionId": "string",
      "slides": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `layouts` | array<object> | The available layouts in the presentation. |
| `locale` | string | The locale of the presentation. |
| `masters` | array<object> | The master slide definitions for the presentation. |
| `pageSize` | object | The size of the presentation pages. |
| `presentationId` | string | The unique ID of the presentation. |
| `revisionId` | string | The current revision ID of the presentation. |
| `slides` | array<object> | The slides in the presentation. |
| `title` | string | The presentation title. |

## Native endpoint

Through the native Google Slides API, this operation is `GET /v1/presentations/:presentationId` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-presentation.md) for the provider-specific parameters and requirements.

