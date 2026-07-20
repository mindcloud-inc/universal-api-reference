# EasyPost: Create Batch Label

Creates a label for an existing batch in EasyPost.

```
PUT https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch-label', {
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
| `id` | string | yes | EasyPost Batch ID, beginning with batch_. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileFormat` | string | no | Optional label file format to create for the batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "labelPdfUrl": "https://example.com",
      "labelUrl": "https://example.com",
      "mode": "string",
      "object": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `labelPdfUrl` | string |  |
| `labelUrl` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `state` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /batches/:id/label` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-label.md) for the provider-specific parameters and requirements.

