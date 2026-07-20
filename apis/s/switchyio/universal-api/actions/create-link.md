# Switchy.io: Create Link

Creates a new link in Switchy.io.

```
POST https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "domain": "hi.switchy.io",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/create-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "domain": "hi.switchy.io",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes |  |
| `domain` | string | yes | Default: `hi.switchy.io`. |
| `id` | string | yes |  |
| `title` | string | no |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "id": "string",
      "showGDPR": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "uniq": 1,
      "url": "https://example.com",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `description` | string |  |
| `domain` | string |  |
| `id` | string |  |
| `showGDPR` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `uniq` | number |  |
| `url` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Switchy.io API, this operation is `POST https://api.switchy.io/v1/links/create` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

