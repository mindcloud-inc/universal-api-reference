# Senja: Create Testimonial

Creates a testimonial in your Senja project.

```
POST https://connect.mindcloud.co/v1/universal/senja/latest/actions/create-testimonial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Senja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/senja/latest/actions/create-testimonial" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/senja/latest/actions/create-testimonial', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | The company name for the testimonial author. |
| `companyRole` | string | no | The job title or role for the testimonial author. |
| `email` | string | no | The email address of the testimonial author. |
| `imageUrl` | string | no | The image URL for the testimonial author. |
| `link` | string | no | A link associated with the testimonial author. |
| `name` | string | yes | The name of the testimonial author. |
| `rating` | number | no | The testimonial rating. |
| `text` | string | no | The testimonial text. |
| `type` | string | no | The testimonial type. |
| `videoUrl` | string | no | The testimonial video URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | ID of the newly created testimonial. |
| `message` | string | Confirmation message returned by Senja after creating a testimonial. |

## Native endpoint

Through the native Senja API, this operation is `POST /testimonials` (base URL `https://api.senja.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-testimonial.md) for the provider-specific parameters and requirements.

