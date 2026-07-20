# Pachca (Admin): List Audit Events

Retrieves audit events from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-audit-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-audit-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-audit-events?${params}`, {
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
| `actorId` | number | no | Filter by actor id. |
| `actorType` | string | no | Filter by actor type. |
| `entityId` | number | no | Filter by entity id. |
| `entityType` | string | no | Filter by entity type. |
| `startTime` | date | no |  |
| `endTime` | date | no |  |
| `eventKey` | string | no |  |
| `limit` | number | no |  |
| `cursor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /audit_events` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audit-events.md) for the provider-specific parameters and requirements.

