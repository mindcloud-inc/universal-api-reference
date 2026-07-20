# Rossum: Export Queue Annotations

Exports annotations from a Rossum queue.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/export-queue-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/export-queue-annotations?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/export-queue-annotations?${params}`, {
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
| `id` | number | yes | Queue ID to export annotations from. |
| `status` | string | no | Annotation status filter for the export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Rossum pagination metadata. |
| `results` | array<object> | Exported queue annotations. |

## Native endpoint

Through the native Rossum API, this operation is `GET /queues/:id/export` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-queue-annotations.md) for the provider-specific parameters and requirements.

