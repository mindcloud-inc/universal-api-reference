# Celigo: List Audit Logs



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-audit-logs?${params}`, {
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
| `resourceType` | list<string> | no | Only return entries for this resource type. One of: `accesstoken`, `agent`, `agentgroup`, `alert`, `api`, `ashare`, `asynchelper`, `connection`, `dataset`, `ediprofile`, `environment`, `export`, `file`, `filedefinition`, `flow`, `folder`, `group`, `iclient`, `idpconfig`, `import`, `integration`, `knowledgebase`, `lookupcache`, `mcpserver`, `networkpolicy`, `notification`, `revision`, `role`, `script`, `ssoclient`, `stack`, `supportshare`, `sync`, `tool`, `topic`, `user`. |
| `resourceId` | string | no | Only return entries for this resource. Requires Resource Type. |
| `action` | list<string> | no | Only return entries for this event. One of: `create`, `delete`, `purge`, `purgelogs`, `restore`, `signin`, `signout`, `update`, `view`. |
| `from` | date | no | Only return entries at or after this time. |
| `to` | date | no | Only return entries at or before this time. Must not be in the future. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `byUserId` | string | no | Only return entries by this user ID, or "support" for Celigo support actions. |
| `source` | list<string> | no | Only return entries from this source. One of: `api`, `cli`, `connector`, `mcp`, `ora`, `script`, `sso`, `stack`, `system`, `ui`. |
| `fieldPath` | string | no | Restrict field changes to this exact field path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Celigo API returns.

## Native endpoint

Through the native Celigo API, this operation is `GET /audit` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audit-logs.md) for the provider-specific parameters and requirements.

