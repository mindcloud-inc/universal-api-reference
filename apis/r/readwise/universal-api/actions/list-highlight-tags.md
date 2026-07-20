# Readwise: List Highlight Tags

Retrieves tags for a Readwise highlight.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-highlight-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-highlight-tags?connectionId=$CONNECTION_ID&highlightId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "highlightId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-highlight-tags?${params}`, {
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
| `highlightId` | number | yes | ID of the highlight whose tags to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v2/highlights/:highlight_id/tags` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-highlight-tags.md) for the provider-specific parameters and requirements.

