# ShortPen: Create Link

Creates a new link in ShortPen.

```
POST https://connect.mindcloud.co/v1/universal/shortPen/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShortPen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortPen/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "domain_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortPen/latest/actions/create-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "domain_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Destination URL that will be shortened. |
| `domain_id` | number | yes | ID of the domain that will host the short link. Use List Domains to find valid IDs. |
| `title` | string | no | Optional human-friendly title for the link. |
| `custom_slug` | string | no | Branded slug to append instead of an auto-generated code. |
| `folder_id` | number | no | Existing folder to assign the link to. Use List Folders to find valid IDs. |
| `generate_qr` | boolean | no | Generate and return a QR code for the new link. |
| `enable_tracking` | boolean | no | Associate the link with a tracking pixel. Requires Pixel ID. |
| `redirect_type` | number | no | HTTP redirect type. Use 301 or 302. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | no | Optional workspace override when the key can access multiple workspaces. |
| `pixel_id` | number | no | Pixel identifier used when tracking is enabled. Use List Pixels to find valid IDs. |
| `link_cloak` | boolean | no | Cloak the destination URL. |
| `hide_referer` | boolean | no | Remove the referrer header for visitors. |
| `with_password` | boolean | no | Protect the link behind a password. |
| `url_password` | string | no | Password required when password protection is enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShortPen API returns.

## Native endpoint

Through the native ShortPen API, this operation is `POST /v1/generate` (base URL `https://api.shortpen.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

