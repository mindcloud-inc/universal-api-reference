# Linkly: Export Links

Retrieves a link export from Linkly.

```
GET https://connect.mindcloud.co/v1/universal/linkly/latest/actions/export-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/export-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkly/latest/actions/export-links?${params}`, {
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
| `search` | string | no | Search query to filter links. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockBots": true,
      "clicksCount": 1,
      "clicksThirtyDays": 1,
      "clicksToday": 1,
      "cloaking": true,
      "deleted": true,
      "domain": "string",
      "enabled": true,
      "forwardParams": true,
      "fullUrl": "https://example.com",
      "id": 1,
      "insertedAt": "string",
      "name": "Ava Chen",
      "note": "string",
      "publicAnalytics": true,
      "rules": [
        {}
      ],
      "slug": "string",
      "spam": true,
      "updatedAt": "string",
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
| `blockBots` | boolean | Whether bots are blocked. |
| `clicksCount` | number | Total click count in the export payload. |
| `clicksThirtyDays` | number | Thirty-day click count. |
| `clicksToday` | number | Today's click count. |
| `cloaking` | boolean | Whether cloaking is enabled. |
| `deleted` | boolean | Whether the link is deleted. |
| `domain` | string | Domain used by the short link. |
| `enabled` | boolean | Whether the link is enabled. |
| `forwardParams` | boolean | Whether query parameters are forwarded. |
| `fullUrl` | string | Shortened Linkly URL. |
| `id` | number | Link ID. |
| `insertedAt` | string | Creation timestamp. |
| `name` | string | Optional link name. |
| `note` | string | Optional internal note. |
| `publicAnalytics` | boolean | Whether public analytics is enabled. |
| `rules` | array<object> | Redirect rule definitions. |
| `slug` | string | Optional slug value when available. |
| `spam` | boolean | Whether the link is marked as spam. |
| `updatedAt` | string | Last update timestamp. |
| `url` | string | Destination URL. |
| `workspaceId` | number | Workspace ID that owns the link. |

## Native endpoint

Through the native Linkly API, this operation is `GET /workspace/:workspace_id/links/export` (base URL `https://app.linklyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-links.md) for the provider-specific parameters and requirements.

