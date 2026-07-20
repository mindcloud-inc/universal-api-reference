# Uniqode: Activate QR Code

Activates a dynamic QR code in Uniqode.

```
PUT https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/activate-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/activate-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrCodeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/activate-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "qrCodeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrCodeId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "campaign_active": true,
        "content_type": 1,
        "created": "2026-05-07T12:00:00.000Z",
        "custom_url": "https://example.com",
        "id": 1,
        "name": "Ava Chen",
        "updated": "2026-05-07T12:00:00.000Z"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "creation_source": "string",
      "domain": 1,
      "heartbeat": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "location_enabled": true,
      "maintainer": 1,
      "name": "Ava Chen",
      "notes": "string",
      "organization": 1,
      "qr_type": 1,
      "scans": 1,
      "spice_migration_completed": true,
      "state": "string",
      "tags": [
        {}
      ],
      "threat_active": true,
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |
| `campaign.campaign_active` | boolean |  |
| `campaign.content_type` | number |  |
| `campaign.created` | date |  |
| `campaign.custom_url` | string |  |
| `campaign.id` | number |  |
| `campaign.name` | string |  |
| `campaign.updated` | date |  |
| `created` | date |  |
| `creation_source` | string |  |
| `domain` | number |  |
| `heartbeat` | date |  |
| `id` | number |  |
| `location_enabled` | boolean |  |
| `maintainer` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `organization` | number |  |
| `qr_type` | number |  |
| `scans` | number |  |
| `spice_migration_completed` | boolean |  |
| `state` | string |  |
| `tags` | array<object> |  |
| `threat_active` | boolean |  |
| `updated` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Uniqode API, this operation is `PUT /qrcodes/:qrCodeId/activate/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-qr-code.md) for the provider-specific parameters and requirements.

