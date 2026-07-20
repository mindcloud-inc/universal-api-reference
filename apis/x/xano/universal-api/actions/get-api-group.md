# Xano: Get API Group

Retrieves an API group from Xano by ID.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-api-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-api-group?connectionId=$CONNECTION_ID&apigroup_id=1&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apigroup_id": "1",
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-api-group?${params}`, {
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
| `apigroup_id` | number | yes | The Xano API group ID. |
| `workspace_id` | number | yes | The Xano workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "canonical": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "docs": "string",
      "guid": "string",
      "id": 1,
      "name": "Ava Chen",
      "swagger": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `canonical` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `docs` | string |  |
| `guid` | string |  |
| `id` | number |  |
| `name` | string |  |
| `swagger` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Xano API, this operation is `GET /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-group.md) for the provider-specific parameters and requirements.

