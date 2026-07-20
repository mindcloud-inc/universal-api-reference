# Shotstack: Direct Upload



```
POST https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/direct-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/direct-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/direct-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "id": "string",
          "url": "https://example.com"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.id` | string | Upload identifier from the attributes object. |
| `data.attributes.url` | string | Signed upload URL returned by Shotstack. |
| `data.id` | string | Upload identifier. |
| `data.type` | string | Resource type for the upload. |

## Native endpoint

Through the native Shotstack API, this operation is `POST /edit/v1/upload` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/direct-upload.md) for the provider-specific parameters and requirements.

