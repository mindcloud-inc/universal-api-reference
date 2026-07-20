# Lunatask: Update Note



```
PUT https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/update-note', {
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
| `id` | string | yes | The ID of the note to update |
| `name` | string | no | The updated note name |
| `content` | string | no | The updated note content in Markdown |
| `notebookId` | string | no | The notebook ID for the note |
| `dateOn` | date | no | The ISO-8601 formatted date assigned to the note |

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

Through the native Lunatask API, this operation is `PUT /notes/:id` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

