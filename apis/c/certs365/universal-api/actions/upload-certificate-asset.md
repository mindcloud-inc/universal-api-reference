# Certs 365: Upload Certificate Asset

Uploads a certificate asset to Certs 365 storage.

```
POST https://connect.mindcloud.co/v1/universal/certs365/latest/actions/upload-certificate-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/upload-certificate-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "certificateNumber": "string",
  "type": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certs365/latest/actions/upload-certificate-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "certificateNumber": "string",
    "type": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Certificate file to upload. |
| `certificateNumber` | string | yes | The ID or number of the certificate. |
| `type` | number | yes | Certificate type: 1 with PDF, 2 without PDF, 3 batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileUrl": "https://example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileUrl` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `POST /api/upload-certificate` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-certificate-asset.md) for the provider-specific parameters and requirements.

