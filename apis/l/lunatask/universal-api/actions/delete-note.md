# Lunatask: Delete Note



```
DELETE https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/delete-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/delete-note?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/delete-note?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the note to delete |

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

Through the native Lunatask API, this operation is `DELETE /notes/:id` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-note.md) for the provider-specific parameters and requirements.

