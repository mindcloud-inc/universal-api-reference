# Trust: List Testimonials

Retrieves testimonials from a Trust workspace.

```
GET https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-testimonials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-testimonials?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-testimonials?${params}`, {
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

Through the native Trust API, this operation is `GET /testimonial/all/:workspaceId` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-testimonials.md) for the provider-specific parameters and requirements.

