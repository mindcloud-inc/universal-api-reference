# Dub: Bulk Create Links

Creates links in Dub in bulk.

```
POST https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-create-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-create-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dub/latest/actions/bulk-create-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `links[]` | array<object> | yes | JSON array of link objects. Each item must include `url`. Common optional keys include `domain`, `key`, `title`, `externalId`, `tagIds`, `tagNames`, `folderId`, `comments`, and `expiresAt`. |
| `links[].url` | string | no | Destination URL for this link row. Required by Dub for each link object. Example: `https://example.com`. |
| `links[].domain` | string | no | Short-link domain for this row. Example: `go.example.com`. |
| `links[].key` | string | no | Custom short-link slug for this row. Example: `launch`. |
| `links[].title` | string | no | Optional title for this row. |
| `links[].externalId` | string | no | External identifier for this row. Example: `crm-123`. |
| `links[].tagIds[]` | array<string> | no | Tag IDs assigned to this row. |
| `links[].tagNames[]` | array<string> | no | Tag names assigned to this row. |
| `links[].folderId` | string | no | Folder ID assigned to this row. |
| `links[].comments` | string | no | Comments for this row. |
| `links[].expiresAt` | date | no | ISO-8601 expiration timestamp for this row. Example: `2026-06-01T12:00:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dub API returns.

## Native endpoint

Through the native Dub API, this operation is `POST /links/bulk` (base URL `https://api.dub.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-links.md) for the provider-specific parameters and requirements.

