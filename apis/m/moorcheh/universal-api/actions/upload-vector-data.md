# Moorcheh: Upload Vector Data

Uploads vector data to a Moorcheh namespace.

```
POST https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/upload-vector-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/upload-vector-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespace_name": "Ava Chen",
  "vectors[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/upload-vector-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespace_name": "Ava Chen",
    "vectors[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace_name` | string | yes | Name of the vector namespace to upload vectors to. |
| `vectors[]` | array<object> | yes | Array of vector objects with id, vector, optional text, and optional metadata fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual_additions": 1,
      "credit_limits": {},
      "execution_time": 1,
      "items_after_upload": 1,
      "message": "string",
      "requested_uploads": 1,
      "status": "string",
      "vector_ids_processed": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual_additions` | number | Number of vectors actually stored. |
| `credit_limits` | object | Plan and item-limit details. |
| `execution_time` | number | Request execution time in seconds. |
| `items_after_upload` | number | Namespace item count after upload. |
| `message` | string | Human-readable upload message. |
| `requested_uploads` | number | Number of vectors requested for upload. |
| `status` | string | Upload status. |
| `vector_ids_processed` | array<string> | Vector IDs processed by Moorcheh. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /namespaces/:namespace_name/vectors` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-vector-data.md) for the provider-specific parameters and requirements.

