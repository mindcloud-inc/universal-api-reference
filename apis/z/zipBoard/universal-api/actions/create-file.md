# zipBoard: Create File

Creates a new file in zipBoard.

```
POST https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "projectId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "projectId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional file description. |
| `name` | string | yes | File display name. |
| `projectId` | string | yes | Project ID where the file should be stored. |
| `url` | string | yes | URL of the file to review. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | File description. |
| `id` | string | File identifier. |
| `name` | string | File name. |
| `projectId` | string | Project identifier. |
| `status` | string | File status. |
| `url` | string | File URL. |

## Native endpoint

Through the native zipBoard API, this operation is `POST /files` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file.md) for the provider-specific parameters and requirements.

