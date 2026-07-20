# Printful: Get Mockup Templates

Retrieves layout templates for Printful mockup generation.

```
GET https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-mockup-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-mockup-templates?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-mockup-templates?${params}`, {
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
| `id` | string | yes | The Printful product variant id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image_url": "https://example.com",
      "placement": "string",
      "template_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image_url` | string |  |
| `placement` | string |  |
| `template_id` | number |  |

## Native endpoint

Through the native Printful API, this operation is `GET /mockup-generator/templates/{id}` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mockup-templates.md) for the provider-specific parameters and requirements.

