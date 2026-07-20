# Discourse: Generate Presigned Put

Generates a presigned upload URL in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/generate-presigned-put
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/generate-presigned-put" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "Ava Chen",
  "file_size": 1,
  "type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/generate-presigned-put', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "Ava Chen",
    "file_size": 1,
    "type": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | Original filename for the direct upload. |
| `file_size` | number | yes | File size in bytes. |
| `type` | string | yes | Upload type. One of: `0`, `1`, `2`, `3`, `4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "signed_headers": {},
      "unique_identifier": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `signed_headers` | object |  |
| `unique_identifier` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /uploads/generate-presigned-put.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-presigned-put.md) for the provider-specific parameters and requirements.

