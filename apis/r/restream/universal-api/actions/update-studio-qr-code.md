# Restream: Update Studio QR Code

Updates a studio QR code in Restream.

```
PUT https://connect.mindcloud.co/v1/universal/restream/latest/actions/update-studio-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/restream/latest/actions/update-studio-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrCodeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restream/latest/actions/update-studio-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "qrCodeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `link` | string | no | Updated QR code destination link. |
| `qrCodeId` | string | yes | The ID of the QR code to update. |
| `title` | string | no | Updated QR code title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brandId": "string",
      "id": "string",
      "link": "https://example.com",
      "shouldShowTitle": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandId` | string |  |
| `id` | string |  |
| `link` | string |  |
| `shouldShowTitle` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Restream API, this operation is `PATCH /user/studio/qr-codes/:qrCodeId` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-studio-qr-code.md) for the provider-specific parameters and requirements.

