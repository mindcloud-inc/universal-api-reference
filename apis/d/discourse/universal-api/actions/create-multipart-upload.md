# Discourse: Create Multipart Upload

Creates a multipart upload in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-multipart-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-multipart-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "Ava Chen",
  "file_size": 1,
  "upload_type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-multipart-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "Ava Chen",
    "file_size": 1,
    "upload_type": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | Original filename for the multipart upload. |
| `file_size` | number | yes | File size in bytes. |
| `upload_type` | string | yes | Upload type. One of: `0`, `1`, `2`, `3`, `4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_upload_identifier": "string",
      "key": "string",
      "unique_identifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_upload_identifier` | string |  |
| `key` | string |  |
| `unique_identifier` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /uploads/create-multipart.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multipart-upload.md) for the provider-specific parameters and requirements.

