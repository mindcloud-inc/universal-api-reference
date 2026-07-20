# Typeflo: Create Post

Creates a new post in Typeflo.

```
POST https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postData.title": "string",
  "postData.content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postData.title": "string",
    "postData.content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postData.title` | string | yes | The title of the post. |
| `postData.content` | string | yes | The main post content in HTML. |
| `postData.slug` | string | no | URL-friendly version of the post title. |
| `postData.author` | string | no | Author ID for the post. |
| `postData.categories[].label` | string | no | Display label for an assigned category. |
| `postData.categories[].value` | string | no | Category ID for an assigned category. |
| `postData.tags[].label` | string | no | Display label for an assigned tag. |
| `postData.tags[].value` | string | no | Tag ID for an assigned tag. |
| `postData.excerpt` | string | no | Short summary or introduction for the post. |
| `postData.metatitle` | string | no | Meta title used in SEO and previews. |
| `postData.metadescription` | string | no | Meta description used in SEO and previews. |
| `postData.publishDate` | string | no | Publish date in DD/MM/YYYY format. |
| `postData.tocStatus` | boolean | no | Whether the table of contents is enabled. |
| `postData.isDraft` | boolean | no | Whether to save the post as a draft. |
| `postData.scheduled` | string | no | Scheduled publish time in DD/MM/YYYY HH:MM AM/PM format, or null. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Typeflo API, this operation is `POST /admin/posts` (base URL `https://{{credentials.subdomain}}.typeflo.io/api/headless`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

