# Zaia: Get Tag

Retrieves a tag from your Zaia workspace.

```
GET https://connect.mindcloud.co/v1/universal/zaia/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/get-tag?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zaia/latest/actions/get-tag?${params}`, {
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
| `id` | string | yes | The UUID of the tag to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeTicketCount": 1,
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeTicketCount` | number | Number of active tickets using the tag. |
| `color` | string | Tag color. |
| `createdAt` | date | Tag creation timestamp. |
| `description` | string | Tag description. |
| `id` | string | Tag UUID. |
| `name` | string | Tag display name. |
| `updatedAt` | date | Tag update timestamp. |
| `workspaceId` | string | Workspace UUID that owns the tag. |

## Native endpoint

Through the native Zaia API, this operation is `GET /api/v1/tags/:id` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

