# Raven Tools: List Links By Tag

Retrieves links by tag from Raven Tools.

```
GET https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-links-by-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-links-by-tag?connectionId=$CONNECTION_ID&domain=mindcloud.co&tag=blogs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "mindcloud.co",
  "tag": "blogs"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-links-by-tag?${params}`, {
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
| `domain` | string | yes | The domain to inspect for link records. Default: `codex-raven-tools-verify-20260408.example`. Example: `mindcloud.co`. |
| `tag` | string | yes | The required tag filter for returned links. Default: `bulk`. Example: `blogs`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_email": "ava@example.com",
      "contact_name": "Ava Chen",
      "cost_frequency": "string",
      "cost_type": "string",
      "date_added": "string",
      "end_date": "string",
      "group_id": "string",
      "link_cost": "https://example.com",
      "link_id": "https://example.com",
      "link_status": "https://example.com",
      "link_text": "https://example.com",
      "link_type": "https://example.com",
      "link_url": "https://example.com",
      "payment_method": "string",
      "payment_reference": "string",
      "start_date": "string",
      "tags": "string",
      "user_id": "string",
      "user_name": "Ava Chen",
      "website_domain": "string",
      "website_type": "string",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_email` | string |  |
| `contact_name` | string |  |
| `cost_frequency` | string |  |
| `cost_type` | string |  |
| `date_added` | string |  |
| `end_date` | string |  |
| `group_id` | string |  |
| `link_cost` | string |  |
| `link_id` | string |  |
| `link_status` | string |  |
| `link_text` | string |  |
| `link_type` | string |  |
| `link_url` | string |  |
| `payment_method` | string |  |
| `payment_reference` | string |  |
| `start_date` | string |  |
| `tags` | string |  |
| `user_id` | string |  |
| `user_name` | string |  |
| `website_domain` | string |  |
| `website_type` | string |  |
| `website_url` | string |  |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-links-by-tag.md) for the provider-specific parameters and requirements.

