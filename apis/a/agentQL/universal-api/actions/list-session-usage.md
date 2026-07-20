# AgentQL: List Session Usage

Retrieves Tetra browser session usage from AgentQL.

```
GET https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/list-session-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AgentQL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/list-session-usage?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/list-session-usage?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subUserId` | string | no |  |
| `sessionId` | string | no |  |
| `startAfter` | date | no |  |
| `endBefore` | date | no |  |
| `status` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AgentQL API returns.

## Native endpoint

Through the native AgentQL API, this operation is `GET /v1/tetra/usage` (base URL `https://api.agentql.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-session-usage.md) for the provider-specific parameters and requirements.

