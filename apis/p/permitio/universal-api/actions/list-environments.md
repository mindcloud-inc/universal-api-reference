# Permit.io: List Environments



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0&projId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-environments?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customBranchName": "Ava Chen",
      "description": "string",
      "emailConfiguration": {},
      "id": "string",
      "jwks": {},
      "key": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "projectId": "string",
      "settings": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customBranchName` | string |  |
| `description` | string |  |
| `emailConfiguration` | object |  |
| `id` | string |  |
| `jwks` | object |  |
| `key` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `settings` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Permit.io API, this operation is `GET /v2/projects/:projId/envs` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

