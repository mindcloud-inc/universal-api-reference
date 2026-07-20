# PostcardMania: Get QR Code Tracking

Retrieves tracking for a PostcardMania QR code.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-qr-code-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-qr-code-tracking?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-qr-code-tracking?${params}`, {
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
| `qrCodeID` | string | no | Internal QR code identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Pagination metadata. |
| `results` | array<object> | QR code tracking records. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /qr-code/{{qrCodeID}}/tracking` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code-tracking.md) for the provider-specific parameters and requirements.

