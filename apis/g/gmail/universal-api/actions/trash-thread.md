# Google Mail: Trash Thread

Moves a Gmail thread to trash.

```
PUT https://connect.mindcloud.co/v1/universal/gmail/latest/actions/trash-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/trash-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "17c7f5f9f1d6c1a2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/trash-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "17c7f5f9f1d6c1a2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Gmail thread ID to move to trash. Example: `17c7f5f9f1d6c1a2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "historyId": "string",
      "id": "string",
      "snippet": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `historyId` | string |  |
| `id` | string |  |
| `snippet` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `POST /threads/:id/trash` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trash-thread.md) for the provider-specific parameters and requirements.

