# WaiverForever: Get Signed Waiver

Retrieves a signed waiver from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-signed-waiver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-signed-waiver?connectionId=$CONNECTION_ID&waiverId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "waiverId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-signed-waiver?${params}`, {
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
| `waiverId` | string | yes | Signed waiver identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "device": {},
      "geolocation": {},
      "hasPdf": true,
      "id": "string",
      "ip": "string",
      "note": "string",
      "pictures": [
        {}
      ],
      "receivedAt": 1,
      "requestId": "string",
      "s3PdfDownloadUrl": "https://example.com",
      "signedAt": 1,
      "status": "string",
      "tags": [
        "string"
      ],
      "templateId": "string",
      "templateTitle": "string",
      "templateVersion": "string",
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Filled waiver fields. |
| `device` | object | Signing device details. |
| `geolocation` | object | Signing geolocation. |
| `hasPdf` | boolean | Whether a PDF is available. |
| `id` | string | Signed waiver identifier. |
| `ip` | string | Signer IP address. |
| `note` | string | Waiver note. |
| `pictures` | array<object> | Pictures attached to the waiver. |
| `receivedAt` | number | Server received timestamp. |
| `requestId` | string | Waiver request identifier if present. |
| `s3PdfDownloadUrl` | string | Temporary PDF download URL when available. |
| `signedAt` | number | Waiver signed timestamp. |
| `status` | string | Waiver status. |
| `tags` | array<string> | Waiver tags. |
| `templateId` | string | Template identifier. |
| `templateTitle` | string | Template title. |
| `templateVersion` | string | Template version. |
| `trackingId` | string | Tracking identifier if present. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v1/waiver/:waiver_id` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signed-waiver.md) for the provider-specific parameters and requirements.

