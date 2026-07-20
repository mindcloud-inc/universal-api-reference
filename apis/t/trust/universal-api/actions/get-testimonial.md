# Trust: Get Testimonial

Retrieves a testimonial from Trust.

```
GET https://connect.mindcloud.co/v1/universal/trust/latest/actions/get-testimonial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/get-testimonial?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trust/latest/actions/get-testimonial?${params}`, {
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
| `id` | string | yes | The testimonial ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerVideos": [
        [
          {}
        ]
      ],
      "company": "string",
      "consentDateTime": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalVideoHtml": "string",
      "firstname": "Ava",
      "gaveConsent": true,
      "id": "string",
      "imageUrl": "https://example.com",
      "lastname": "Chen",
      "published": true,
      "socialMediaProfiles": [
        [
          "string"
        ]
      ],
      "stars": 1,
      "subtitle": "string",
      "testimonialText": "string",
      "title": "string",
      "videoUrl": "https://example.com",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerVideos[]` | array<object> |  |
| `company` | string |  |
| `consentDateTime` | date |  |
| `created` | date |  |
| `email` | string |  |
| `externalVideoHtml` | string |  |
| `firstname` | string |  |
| `gaveConsent` | boolean |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `lastname` | string |  |
| `published` | boolean |  |
| `socialMediaProfiles[]` | array<string> |  |
| `stars` | number |  |
| `subtitle` | string |  |
| `testimonialText` | string |  |
| `title` | string |  |
| `videoUrl` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `GET /testimonial/:id` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-testimonial.md) for the provider-specific parameters and requirements.

