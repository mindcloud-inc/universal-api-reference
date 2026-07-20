# Xano: Create API

Creates a new API endpoint in Xano.

```
POST https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apigroup_id": 1,
  "description": "string",
  "name": "Ava Chen",
  "verb": "string",
  "workspace_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-api', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apigroup_id": 1,
    "description": "string",
    "name": "Ava Chen",
    "verb": "string",
    "workspace_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apigroup_id` | number | yes | The Xano API group ID. |
| `description` | string | yes | API endpoint description. |
| `name` | string | yes | API endpoint name. |
| `verb` | string | yes | HTTP verb for the endpoint. |
| `workspace_id` | number | yes | The Xano workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth": true,
      "cache": {
        "active": true,
        "auth": true,
        "datasource": true,
        "input": true,
        "ip": true,
        "ttl": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "docs": "string",
      "guid": "string",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verb": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | boolean |  |
| `cache.active` | boolean |  |
| `cache.auth` | boolean |  |
| `cache.datasource` | boolean |  |
| `cache.input` | boolean |  |
| `cache.ip` | boolean |  |
| `cache.ttl` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `docs` | string |  |
| `guid` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `verb` | string |  |

## Native endpoint

Through the native Xano API, this operation is `POST /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api.md) for the provider-specific parameters and requirements.

