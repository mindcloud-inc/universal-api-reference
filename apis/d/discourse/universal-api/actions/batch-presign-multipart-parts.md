# Discourse: Batch Presign Multipart Parts

Generates presigned URLs for multipart upload parts in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/batch-presign-multipart-parts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/batch-presign-multipart-parts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "part_numbers": "string",
  "unique_identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/batch-presign-multipart-parts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "part_numbers": "string",
    "unique_identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `part_numbers` | string | yes | Multipart part numbers to presign. |
| `unique_identifier` | string | yes | The unique identifier returned by Create Multipart Upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "presigned_urls": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `presigned_urls` | object |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /uploads/batch-presign-multipart-parts.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-presign-multipart-parts.md) for the provider-specific parameters and requirements.

