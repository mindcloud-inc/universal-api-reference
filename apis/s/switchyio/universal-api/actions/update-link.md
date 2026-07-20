# Switchy.io: Update Link

Updates an existing link in Switchy.io.

```
PUT https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string",
  "id": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string",
    "id": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes |  |
| `id` | string | yes |  |
| `url` | string | yes |  |
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
      "removed": "2026-05-07T12:00:00.000Z",
      "showGDPR": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "uniq": 1,
      "url": "https://example.com"
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
| `removed` | date |  |
| `showGDPR` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `uniq` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Switchy.io API, this operation is `PUT https://api.switchy.io/v1/links/by-domain/:domain/:id` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

