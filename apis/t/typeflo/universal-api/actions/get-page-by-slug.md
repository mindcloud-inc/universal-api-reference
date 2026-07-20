# Typeflo: Get Page By Slug

Retrieves a static page from Typeflo by slug.

```
GET https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-page-by-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-page-by-slug?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-page-by-slug?${params}`, {
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
| `slug` | string | yes | The unique slug of the page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "docsid": "string",
      "id": "string",
      "isDraft": true,
      "metadescription": "string",
      "metatitle": "string",
      "postedby": "string",
      "slug": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `createdAt` | date |  |
| `docsid` | string |  |
| `id` | string |  |
| `isDraft` | boolean |  |
| `metadescription` | string |  |
| `metatitle` | string |  |
| `postedby` | string |  |
| `slug` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Typeflo API, this operation is `GET /content/pages/:slug` (base URL `https://{{credentials.subdomain}}.typeflo.io/api/headless`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-by-slug.md) for the provider-specific parameters and requirements.

