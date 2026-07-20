# Superthread: Create Note



```
POST https://connect.mindcloud.co/v1/universal/superthread/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "title": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superthread/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "title": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Workspace ID for the Superthread workspace. |
| `title` | string | yes |  |
| `content` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "note": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `note` | object |  |

## Native endpoint

Through the native Superthread API, this operation is `POST /:team_id/notes` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

