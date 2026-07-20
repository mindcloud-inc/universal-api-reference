# Permit.io: Create Tenant



```
POST https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-tenant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-tenant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projId": "string",
  "envId": "string",
  "key": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-tenant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projId": "string",
    "envId": "string",
    "key": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projId` | string | yes | Permit project identifier or key. |
| `envId` | string | yes | Permit environment identifier or key. |
| `key` | string | yes | Unique tenant key within the Permit environment. |
| `name` | string | yes | Tenant display name. |
| `description` | string | no | Tenant description. |
| `attributes` | object | no | Custom tenant attributes object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "environmentId": "string",
      "id": "string",
      "key": "string",
      "lastActionAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "organizationId": "string",
      "projectId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `createdAt` | date |  |
| `description` | string |  |
| `environmentId` | string |  |
| `id` | string |  |
| `key` | string |  |
| `lastActionAt` | date |  |
| `name` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Permit.io API, this operation is `POST /v2/facts/:projId/:envId/tenants` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tenant.md) for the provider-specific parameters and requirements.

