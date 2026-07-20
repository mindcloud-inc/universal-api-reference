# Trust: Update Testimonial

Updates an existing testimonial in Trust.

```
PUT https://connect.mindcloud.co/v1/universal/trust/latest/actions/update-testimonial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trust/latest/actions/update-testimonial" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trust/latest/actions/update-testimonial', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | Company of the testimonial giver. |
| `consentDateTime` | date | no | Date and time when consent was given. |
| `email` | string | no | Email address of the testimonial giver. |
| `externalVideoHtml` | string | no | Embeddable external video HTML. |
| `firstname` | string | no | First name of the testimonial giver. |
| `gaveConsent` | boolean | no | Whether the giver consented to publication. |
| `id` | string | yes | The testimonial ID. |
| `imageUrl` | string | no | Image URL for the testimonial giver. |
| `lastname` | string | no | Last name of the testimonial giver. |
| `published` | boolean | no | Whether the testimonial is published. |
| `socialMediaProfiles` | string | no | List of social media profile URLs. |
| `stars` | number | no | Star rating for the testimonial. |
| `subtitle` | string | no | Subtitle of the testimonial. |
| `testimonialText` | string | no | Text content of the testimonial. |
| `title` | string | no | Title of the testimonial. |
| `videoToken` | string | no | Token of an uploaded video. |
| `videoUrl` | string | no | URL of an uploaded video. |
| `workspaceId` | string | yes | The Trust workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "questionsAndAnswers": "string",
      "socialMediaProfiles": "string",
      "stars": 1,
      "subtitle": "string",
      "testimonialText": "string",
      "title": "string",
      "videoVideoUrl": "https://example.com",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
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
| `questionsAndAnswers` | string |  |
| `socialMediaProfiles` | string |  |
| `stars` | number |  |
| `subtitle` | string |  |
| `testimonialText` | string |  |
| `title` | string |  |
| `videoVideoUrl` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `PUT /testimonial/:id` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-testimonial.md) for the provider-specific parameters and requirements.

