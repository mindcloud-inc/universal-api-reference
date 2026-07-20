# Zaia: Create Tag

Creates a new tag in Zaia.

```
POST https://connect.mindcloud.co/v1/universal/zaia/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "color": "0",
  "description": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zaia/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "color": "0",
    "description": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | list | yes | The color of the tag. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `description` | string | yes | The description of the tag. |
| `name` | string | yes | The display name of the tag. |

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
| `color` | string | Created tag color. |
| `createdAt` | date | Tag creation timestamp. |
| `description` | string | Created tag description. |
| `id` | string | Created tag UUID. |
| `name` | string | Created tag display name. |
| `updatedAt` | date | Tag update timestamp. |
| `workspaceId` | string | Workspace UUID that owns the tag. |

## Native endpoint

Through the native Zaia API, this operation is `POST /api/v1/tags` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

