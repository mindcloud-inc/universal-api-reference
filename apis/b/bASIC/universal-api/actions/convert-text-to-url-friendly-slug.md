# BASIC: Convert text to URL-friendly slug

Converts text to a URL-friendly slug in BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/convert-text-to-url-friendly-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/convert-text-to-url-friendly-slug?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/convert-text-to-url-friendly-slug?${params}`, {
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
| `slug` | string | yes | Text to convert into a URL-friendly slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `slug` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /utils/slugify` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-to-url-friendly-slug.md) for the provider-specific parameters and requirements.

