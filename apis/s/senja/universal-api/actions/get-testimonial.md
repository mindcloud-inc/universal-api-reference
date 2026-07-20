# Senja: Get Testimonial

Retrieves a testimonial from Senja by ID.

```
GET https://connect.mindcloud.co/v1/universal/senja/latest/actions/get-testimonial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Senja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/senja/latest/actions/get-testimonial?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/senja/latest/actions/get-testimonial?${params}`, {
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
| `id` | string | yes | The Senja testimonial ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "testimonial": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `testimonial` | object | The testimonial returned by Senja for the requested ID. |

## Native endpoint

Through the native Senja API, this operation is `GET /testimonials/:id` (base URL `https://api.senja.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-testimonial.md) for the provider-specific parameters and requirements.

