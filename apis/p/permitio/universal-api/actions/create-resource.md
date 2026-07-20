# Permit.io: Create Resource



```
POST https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projId": "string",
  "envId": "string",
  "key": "string",
  "name": "Ava Chen",
  "actions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-resource', {
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
    "name": "Ava Chen",
    "actions": {}
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
| `key` | string | yes | Unique resource key within the Permit environment. |
| `name` | string | yes | Resource display name. |
| `urn` | string | no | Resource URN. |
| `description` | string | no | Resource description. |
| `actions` | object | yes | Actions definition object for the resource. |
| `typeAttributes` | object | no | Type attributes object for the resource. |
| `attributes` | object | no | Custom resource attributes object. |
| `roles` | object | no | Roles definition object for the resource. |
| `relations` | object | no | Relations definition object for the resource. |
| `v1compatPath` | string | no | Legacy v1 compatibility path. |
| `v1compatType` | string | no | Legacy v1 compatibility type. |
| `v1compatName` | string | no | Legacy v1 compatibility name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionGroups": {},
      "actions": {},
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "environmentId": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "projectId": "string",
      "relations": {},
      "roles": {},
      "typeAttributes": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urn": "string",
      "v1compatName": "Ava Chen",
      "v1compatPath": "string",
      "v1compatType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionGroups` | object |  |
| `actions` | object |  |
| `attributes` | object |  |
| `createdAt` | date |  |
| `description` | string |  |
| `environmentId` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `relations` | object |  |
| `roles` | object |  |
| `typeAttributes` | object |  |
| `updatedAt` | date |  |
| `urn` | string |  |
| `v1compatName` | string |  |
| `v1compatPath` | string |  |
| `v1compatType` | string |  |

## Native endpoint

Through the native Permit.io API, this operation is `POST /v2/schema/:projId/:envId/resources` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-resource.md) for the provider-specific parameters and requirements.

