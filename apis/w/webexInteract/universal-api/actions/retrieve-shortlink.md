# Webex Interact: Retrieve shortlink

Retrieves a shortlink from Webex Interact.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-shortlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-shortlink?connectionId=$CONNECTION_ID&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-shortlink?${params}`, {
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
| `linkId` | string | yes | Shortlink ID to retrieve. |

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

Through the native Webex Interact API, this operation is `GET /assets/v1/shortlink/{linkId}` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-shortlink.md) for the provider-specific parameters and requirements.

