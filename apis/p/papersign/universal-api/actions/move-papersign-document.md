# Papersign: Move Papersign Document



```
PUT https://connect.mindcloud.co/v1/universal/papersign/latest/actions/move-papersign-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papersign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/move-papersign-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papersign/latest/actions/move-papersign-document', {
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
| `id` | string | yes | The Papersign document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "document": {
          "completed_at_utc": "2026-05-07T12:00:00.000Z",
          "created_at_utc": "2026-05-07T12:00:00.000Z",
          "folder": {
            "id": 1,
            "name": "Ava Chen",
            "space_id": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "sent_at_utc": "2026-05-07T12:00:00.000Z",
          "space": {
            "id": 1,
            "name": "Ava Chen"
          },
          "status": "string",
          "updated_at_utc": "2026-05-07T12:00:00.000Z"
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results.document.completed_at_utc` | date | The time the document was completed. |
| `results.document.created_at_utc` | date | The time the document was created. |
| `results.document.folder.id` | number | The unique identifier of the folder. |
| `results.document.folder.name` | string | The name of the folder. |
| `results.document.folder.space_id` | number | The unique identifier of the space that owns the folder. |
| `results.document.id` | string | The unique identifier of the document. |
| `results.document.name` | string | The name of the document. |
| `results.document.sent_at_utc` | date | The time the document was sent. |
| `results.document.space.id` | number | The unique identifier of the space. |
| `results.document.space.name` | string | The name of the space. |
| `results.document.status` | string | The status of the document. |
| `results.document.updated_at_utc` | date | The time the document was last updated. |
| `status` | string | Response status. |

## Native endpoint

Through the native Papersign API, this operation is `POST /papersign/documents/:id/move` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-papersign-document.md) for the provider-specific parameters and requirements.

