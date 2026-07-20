# Lunatask: Create Note



```
POST https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notebookId` | string | no | The Notebook ID of the notebook where the note should be created |
| `name` | string | no | The name of the note |
| `content` | string | no | The content of the note in Markdown |
| `dateOn` | date | no | A date assigned to the note |
| `source` | string | no | Identification of the external system where the note is coming from |
| `sourceId` | string | no | The ID of the record in the external system |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "notebookId": "string",
      "pinned": true,
      "sources": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `dateOn` | date |  |
| `id` | string |  |
| `notebookId` | string |  |
| `pinned` | boolean |  |
| `sources` | array |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunatask API, this operation is `POST /notes` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

