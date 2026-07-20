# WaiverForever: Get Sample Waiver

Retrieves a sample waiver from a WaiverForever template.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-sample-waiver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-sample-waiver?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-sample-waiver?${params}`, {
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
| `templateId` | string | yes | WaiverForever template identifier. |

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
| `id` | string | Sample waiver identifier. |
| `ip` | string | Signer IP address. |
| `note` | string | Waiver note when present. |
| `pictures` | array<object> | Pictures attached to the waiver. |
| `receivedAt` | number | Server received timestamp. |
| `s3PdfDownloadUrl` | string | Temporary PDF download URL when available. |
| `signedAt` | number | Waiver signed timestamp. |
| `status` | string | Waiver status when present. |
| `tags` | array<string> | Waiver tags when present. |
| `templateId` | string | Template identifier. |
| `templateTitle` | string | Template title. |
| `templateVersion` | string | Template version. |
| `trackingId` | string | Tracking identifier if present. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v1/template/:template_id/getSampleWaiver` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample-waiver.md) for the provider-specific parameters and requirements.

