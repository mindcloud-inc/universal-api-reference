# Webex Interact: Create shortlink

Creates a new shortlink in Webex Interact.

```
POST https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-shortlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-shortlink" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "target_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-shortlink', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "target_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Shortlink title. |
| `target_url` | string | yes | Destination URL for the shortlink. |
| `tags` | list<string> | no | Optional array of tag strings. |
| `track_clicks` | boolean | no | Whether to track clicks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "link_id": "https://example.com",
      "short_link_url": "https://example.com",
      "tags": [
        "string"
      ],
      "target_url": "https://example.com",
      "title": "string",
      "track_clicks": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `link_id` | string |  |
| `short_link_url` | string |  |
| `tags` | array<string> |  |
| `target_url` | string |  |
| `title` | string |  |
| `track_clicks` | boolean |  |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /assets/v1/shortlink` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shortlink.md) for the provider-specific parameters and requirements.

