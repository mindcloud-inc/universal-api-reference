# Zaia: Update Tag

Updates an existing tag in Zaia.

```
PUT https://connect.mindcloud.co/v1/universal/zaia/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zaia/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The UUID of the tag to update. |
| `color` | list | no | The color of the tag. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `description` | string | no | The description of the tag. |
| `name` | string | no | The display name of the tag. |

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
| `color` | string | Updated tag color. |
| `createdAt` | date | Tag creation timestamp. |
| `description` | string | Updated tag description. |
| `id` | string | Updated tag UUID. |
| `name` | string | Updated tag display name. |
| `updatedAt` | date | Tag update timestamp. |
| `workspaceId` | string | Workspace UUID that owns the tag. |

## Native endpoint

Through the native Zaia API, this operation is `PATCH /api/v1/tags/:id` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

