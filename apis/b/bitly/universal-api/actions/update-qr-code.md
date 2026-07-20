# Bitly: Update QR Code

Updates an existing QR code in Bitly.

```
PUT https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrcodeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "qrcodeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrcodeId` | string | yes |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created": "string",
      "groupGuid": "string",
      "longUrls": [
        "https://example.com"
      ],
      "qrcodeId": "string",
      "qrCodeType": "string",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created` | string |  |
| `groupGuid` | string |  |
| `longUrls[]` | string |  |
| `qrcodeId` | string |  |
| `qrCodeType` | string |  |
| `title` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `PATCH /qr-codes/:qrcode_id` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-qr-code.md) for the provider-specific parameters and requirements.

