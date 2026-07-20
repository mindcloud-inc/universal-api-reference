# Permit.io: List Roles



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-roles?connectionId=$CONNECTION_ID&limit=25&offset=0&projId=string&envId=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-roles?${params}`, {
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
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "environmentId": "string",
      "extends": [
        "string"
      ],
      "grantedTo": {},
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "permissions": [
        "string"
      ],
      "projectId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "v1compatAttributes": {},
      "v1compatSettings": {}
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
| `extends` | array<string> |  |
| `grantedTo` | object |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `permissions` | array<string> |  |
| `projectId` | string |  |
| `updatedAt` | date |  |
| `v1compatAttributes` | object |  |
| `v1compatSettings` | object |  |

## Native endpoint

Through the native Permit.io API, this operation is `GET /v2/schema/:projId/:envId/roles` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

