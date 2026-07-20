# Permit.io: List Audit Logs



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&projId=string&envId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projId": "string",
  "envId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-audit-logs?${params}`, {
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
| `projId` | string | yes | Permit project identifier or key. |
| `envId` | string | yes | Permit environment identifier or key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "context": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "decision": true,
      "envId": "string",
      "id": "string",
      "input": {},
      "orgId": "string",
      "pdpConfigId": "string",
      "projectId": "string",
      "query": "string",
      "rawData": {},
      "reason": "string",
      "resourceType": "string",
      "result": {},
      "tenant": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userEmail": "ava@example.com",
      "userKey": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `context` | object |  |
| `createdAt` | date |  |
| `decision` | boolean |  |
| `envId` | string |  |
| `id` | string |  |
| `input` | object |  |
| `orgId` | string |  |
| `pdpConfigId` | string |  |
| `projectId` | string |  |
| `query` | string |  |
| `rawData` | object |  |
| `reason` | string |  |
| `resourceType` | string |  |
| `result` | object |  |
| `tenant` | string |  |
| `timestamp` | date |  |
| `userEmail` | string |  |
| `userKey` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Permit.io API, this operation is `GET /v2/pdps/:projId/:envId/audit_logs` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audit-logs.md) for the provider-specific parameters and requirements.

