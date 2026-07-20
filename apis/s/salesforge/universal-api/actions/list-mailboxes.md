# Salesforge: List Mailboxes

Retrieves mailboxes from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=wks_989gtkhm1ir6z8hdv3gjn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "wks_989gtkhm1ir6z8hdv3gjn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-mailboxes?${params}`, {
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
| `workspaceId` | string | yes | Example: `wks_989gtkhm1ir6z8hdv3gjn`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statuses[]` | array<string> | no | Example: `active`. |
| `mailboxIds[]` | array<string> | no | Example: `mbx_123`. |
| `excludedMailboxIds[]` | array<string> | no | Example: `mbx_456`. |
| `search` | string | no | Example: `sales@mindcloud.co`. |
| `tagIds[]` | array<string> | no | Example: `tag_123`. |
| `notTagIds[]` | array<string> | no | Example: `tag_456`. |
| `addresses[]` | array<string> | no | Example: `sales@mindcloud.co`. |
| `statusCriteria` | string | no | Example: `include_any`. |
| `statusesCriteria[]` | array<string> | no | Example: `active`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/mailboxes` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mailboxes.md) for the provider-specific parameters and requirements.

