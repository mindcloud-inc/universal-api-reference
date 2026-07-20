# Readwise: Add Highlight Tag

Creates a new tag for a Readwise highlight.

```
POST https://connect.mindcloud.co/v1/universal/readwise/latest/actions/add-highlight-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/add-highlight-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "highlightId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/add-highlight-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "highlightId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `highlightId` | number | yes | The Readwise highlight ID to tag. |
| `name` | string | yes | The tag name to add to the highlight. |

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

Through the native Readwise API, this operation is `POST /api/v2/highlights/:highlightId/tags/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-highlight-tag.md) for the provider-specific parameters and requirements.

