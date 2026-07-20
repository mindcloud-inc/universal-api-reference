# Permit.io: Get Role



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-role?connectionId=$CONNECTION_ID&projId=string&envId=string&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projId": "string",
  "envId": "string",
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-role?${params}`, {
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
| `roleId` | string | yes | Permit role identifier. |

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

Through the native Permit.io API, this operation is `GET /v2/schema/:projId/:envId/roles/:roleId` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-role.md) for the provider-specific parameters and requirements.

