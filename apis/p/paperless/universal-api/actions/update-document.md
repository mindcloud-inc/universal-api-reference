# Paperless: Update Document



```
PUT https://connect.mindcloud.co/v1/universal/paperless/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paperless/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Paperless document ID. |
| `name` | string | no | The new name for the document. |
| `state` | string | no | The target document state. |
| `settings` | object | no | The full settings object to apply to the document. |
| `reminderSettings` | object | no | Reminder configuration for the document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Paperless API, this operation is `PATCH /documents/:id` (base URL `https://app.paperless.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

