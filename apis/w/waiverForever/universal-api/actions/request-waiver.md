# WaiverForever: Request Waiver

Creates a waiver request link from a WaiverForever template.

```
POST https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/request-waiver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/request-waiver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/request-waiver', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | WaiverForever template identifier. |
| `ttl` | number | no | Requested waiver expiration time in seconds. Defaults to 86400 when omitted. Example: `86400`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestWaiverUrl": "https://example.com",
      "trackingId": "string",
      "ttl": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestWaiverUrl` | string | Signing URL for the requested waiver. |
| `trackingId` | string | Tracking id for the requested waiver. |
| `ttl` | number | Expiration time in seconds. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v1/template/:template_id/requestWaiver` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-waiver.md) for the provider-specific parameters and requirements.

