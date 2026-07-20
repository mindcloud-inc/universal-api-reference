# Frontegg: Create Role

Creates a new role in Frontegg.

```
POST https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "name": "Ava Chen",
  "level": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "name": "Ava Chen",
    "level": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | Role key. |
| `name` | string | yes | Role name. |
| `description` | string | no | Role description. |
| `isDefault` | boolean | no | Assign this role by default to new users when no roles are specified. |
| `migrateRole` | boolean | no | Assign this role to all users when used with Is Default. |
| `firstUserRole` | boolean | no | Assign this role to the first user in new tenants. |
| `level` | number | yes | Role level; lower numbers are stronger roles. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frontegg API returns.

## Native endpoint

Through the native Frontegg API, this operation is `POST /identity/resources/roles/v1` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-role.md) for the provider-specific parameters and requirements.

