# Google Slides: Create Presentation

Creates a new presentation in Google Slides.

```
POST https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-presentation', {
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
| `title` | string | no | The title for the new presentation. |

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
| `presentationId` | string | The unique ID of the created presentation. |
| `revisionId` | string | The current revision ID of the presentation. |
| `slides` | array<object> | The slides in the presentation. |
| `title` | string | The presentation title. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /v1/presentations` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-presentation.md) for the provider-specific parameters and requirements.

