# Mode: Retrieve Audit Logs

Retrieve audit log events for a Mode workspace.

```
GET https://connect.mindcloud.co/v1/universal/mode/latest/actions/retrieve-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/retrieve-audit-logs?connectionId=$CONNECTION_ID&startTimestamp=2026-04-15T00%3A00%3A00Z&endTimestamp=2026-04-15T18%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startTimestamp": "2026-04-15T00:00:00Z",
  "endTimestamp": "2026-04-15T18:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/retrieve-audit-logs?${params}`, {
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
| `startTimestamp` | string | yes | Start of the audit-log time range in ISO 8601 format. Example: `2026-04-15T00:00:00Z`. |
| `endTimestamp` | string | yes | End of the audit-log time range in ISO 8601 format. Example: `2026-04-15T18:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "actor": {},
      "context": {},
      "description": "string",
      "entity": {},
      "id": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "workspaceUsername": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Action performed. |
| `actor` | object | Actor metadata. |
| `context` | object | Event context object. |
| `description` | string | Audit event description. |
| `entity` | object | Affected entity metadata. |
| `id` | string | Audit log event ID. |
| `timestamp` | date | Event timestamp. |
| `workspaceUsername` | string | Workspace username. |

## Native endpoint

Through the native Mode API, this operation is `GET /audit_logs` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-audit-logs.md) for the provider-specific parameters and requirements.

