# zipBoard: Update File

Updates an existing file in zipBoard.

```
PUT https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-file', {
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
| `description` | string | no | Updated file description. |
| `id` | string | yes | File record ID to update. |
| `name` | string | no | Updated file name. |
| `url` | string | no | Updated review URL. |

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

Through the native zipBoard API, this operation is `PUT /files/:id` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file.md) for the provider-specific parameters and requirements.

