# 4HSE: Create Incident

Creates a new incident in 4HSE.

```
POST https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "dateIncident": "2026-05-07T12:00:00.000Z",
  "subtenantId": "string",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "dateIncident": "2026-05-07T12:00:00.000Z",
    "subtenantId": "string",
    "tenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Title or name of the incident. |
| `dateIncident` | date | yes | Date when the incident occurred. |
| `category` | string | no | Incident category. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `subtenantId` | string | yes | The office where the incident occurred. |
| `tenantId` | string | yes | The project the incident belongs to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | no | Identifier code. |
| `descriptionEvent` | string | no | Description of what happened. |
| `status` | string | no | Workflow status. One of: `0`, `1`, `2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/incident/create` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident.md) for the provider-specific parameters and requirements.

