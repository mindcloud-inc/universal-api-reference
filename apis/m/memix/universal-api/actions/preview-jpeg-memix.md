# Memix: Preview JPEG Memix

Retrieves a JPEG preview from Memix.

```
GET https://connect.mindcloud.co/v1/universal/memix/latest/actions/preview-jpeg-memix
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memix/latest/actions/preview-jpeg-memix?connectionId=$CONNECTION_ID&template_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memix/latest/actions/preview-jpeg-memix?${params}`, {
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
| `template_slug` | string | yes | Memix template slug. |
| `text` | string | no | Text rendered into the preview when the template supports it. |
| `image_url` | string | no | Source image URL used when the template supports image input. |
| `image_id` | string | no | Memix image identifier used when the template supports image input. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Memix API returns.

## Native endpoint

Through the native Memix API, this operation is `GET /preview/memix-:template_slug.jpeg` (base URL `https://api.memix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-jpeg-memix.md) for the provider-specific parameters and requirements.

