# Zenkit: Get Users For Workspace

Retrieves users for a Zenkit workspace.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-users-for-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-users-for-workspace?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-users-for-workspace?${params}`, {
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
| `workspaceId` | string | yes | The workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayname": "Ava Chen",
      "emailCount": 1,
      "fullname": "Ava Chen",
      "id": 1,
      "imageLink": "https://example.com",
      "initials": "string",
      "isImagePreferred": true,
      "organizationId": 1,
      "registered_at": "2026-05-07T12:00:00.000Z",
      "roleId": "string",
      "shortId": "string",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayname` | string |  |
| `emailCount` | number |  |
| `fullname` | string |  |
| `id` | number |  |
| `imageLink` | string |  |
| `initials` | string |  |
| `isImagePreferred` | boolean |  |
| `organizationId` | number |  |
| `registered_at` | date |  |
| `roleId` | string |  |
| `shortId` | string |  |
| `username` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `GET /workspaces/:workspaceId/users` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-users-for-workspace.md) for the provider-specific parameters and requirements.

