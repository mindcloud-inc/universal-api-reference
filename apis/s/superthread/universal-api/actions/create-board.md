# Superthread: Create Board



```
POST https://connect.mindcloud.co/v1/universal/superthread/latest/actions/create-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "projectId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superthread/latest/actions/create-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "projectId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Workspace ID for the Superthread workspace. |
| `projectId` | string | yes | Space ID to add the board to. |
| `title` | string | yes | Board title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board` | object |  |

## Native endpoint

Through the native Superthread API, this operation is `POST /:team_id/boards` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-board.md) for the provider-specific parameters and requirements.

