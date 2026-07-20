# Permit.io: Get Project



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-project?connectionId=$CONNECTION_ID&projId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-project?${params}`, {
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
      "activePolicyRepoId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "settings": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urnNamespace": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activePolicyRepoId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `settings` | object |  |
| `updatedAt` | date |  |
| `urnNamespace` | string |  |

## Native endpoint

Through the native Permit.io API, this operation is `GET /v2/projects/:projId` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

