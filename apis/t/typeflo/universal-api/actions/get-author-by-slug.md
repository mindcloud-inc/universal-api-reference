# Typeflo: Get Author By Slug

Retrieves an author profile from Typeflo by slug.

```
GET https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-author-by-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-author-by-slug?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-author-by-slug?${params}`, {
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
| `slug` | string | yes | The unique slug of the author. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "metadescription": "string",
      "slug": "string",
      "socials": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the author record was created. |
| `description` | string | Author bio or description. |
| `id` | string | The unique ID of the author. |
| `metadescription` | string | Meta description for the author. |
| `slug` | string | The unique slug of the author. |
| `socials` | object | Social profile metadata for the author when configured. |

## Native endpoint

Through the native Typeflo API, this operation is `GET /content/authors/:slug` (base URL `https://{{credentials.subdomain}}.typeflo.io/api/headless`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-author-by-slug.md) for the provider-specific parameters and requirements.

