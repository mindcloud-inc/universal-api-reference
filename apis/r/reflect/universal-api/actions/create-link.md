# Reflect: Create Link

Creates a new link in a Reflect graph.

```
POST https://connect.mindcloud.co/v1/universal/reflect/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reflect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "graphId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reflect/latest/actions/create-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "graphId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `graphId` | list<string> | yes | Your graph identifier |
| `url` | string | yes |  |
| `title` | string | no |  |
| `description` | string | no |  |
| `highlights[]` | array<string> | no | List of highlighted text snippets |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "highlights": [
        "string"
      ],
      "id": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `highlights` | array<string> |  |
| `id` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Reflect API, this operation is `POST /graphs/:graphId/links` (base URL `https://reflect.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

