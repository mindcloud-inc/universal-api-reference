# ME-QR: Get Map QR

Retrieves a map QR code from ME-QR.

```
GET https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/get-map-qr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ME-QR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/get-map-qr?connectionId=$CONNECTION_ID&entryUID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entryUID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/get-map-qr?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entryUID` | string | yes | ID or unique entry key for the QR code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "designType": "string",
      "qrFieldsData": {},
      "qrFolderOptions": {},
      "qrFrame": {},
      "qrOptions": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `designType` | string |  |
| `qrFieldsData` | object |  |
| `qrFolderOptions` | object |  |
| `qrFrame` | object |  |
| `qrOptions` | object |  |
| `title` | string |  |

## Native endpoint

Through the native ME-QR API, this operation is `GET /api/v2/qr/map/:entryUID` (base URL `https://me-qr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map-qr.md) for the provider-specific parameters and requirements.

