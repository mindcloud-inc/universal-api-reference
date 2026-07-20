# ReadyCloud Suite: Create Note

Creates a new note in ReadyCloud Suite.

```
POST https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReadyCloud Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderPk": "string",
  "orgPk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderPk": "string",
    "orgPk": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderPk` | string | yes | ReadyCloud order identifier. |
| `orgPk` | string | yes | ReadyCloud organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "author": {},
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `author` | object |  |
| `content` | string |  |
| `created_at` | date |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native ReadyCloud Suite API, this operation is `POST /api/v2/orgs/:orgPk/orders/:orderPk/notes/` (base URL `https://www.readycloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

