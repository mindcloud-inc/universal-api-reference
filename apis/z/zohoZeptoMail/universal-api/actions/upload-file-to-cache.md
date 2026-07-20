# Zoho ZeptoMail: Upload File to Cache

Uploads a file to the Zoho ZeptoMail cache.

```
POST https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/upload-file-to-cache
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/upload-file-to-cache" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/upload-file-to-cache', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "data": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the file being uploaded to ZeptoMail file cache. |
| `data` | string | yes | Binary or text payload to upload to file cache. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "code": "string",
          "message": "string"
        }
      ],
      "file_cache_key": "string",
      "message": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].code` | string |  |
| `data[].message` | string |  |
| `file_cache_key` | string |  |
| `message` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `POST files` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-to-cache.md) for the provider-specific parameters and requirements.

