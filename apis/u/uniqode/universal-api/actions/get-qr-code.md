# Uniqode: Get QR Code

Retrieves a QR code from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-qr-code?connectionId=$CONNECTION_ID&qrCodeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrCodeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-qr-code?${params}`, {
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
| `qrCodeId` | number | yes | The Uniqode QR code ID. |

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
      "cdn_cache": true,
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
      "organization_details": {
        "id": 1,
        "name": "Ava Chen"
      },
      "owner_details": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen"
      },
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
| `cdn_cache` | boolean |  |
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
| `organization_details` | object |  |
| `organization_details.id` | number |  |
| `organization_details.name` | string |  |
| `owner_details` | object |  |
| `owner_details.email` | string |  |
| `owner_details.first_name` | string |  |
| `owner_details.id` | number |  |
| `owner_details.last_name` | string |  |
| `qr_type` | number |  |
| `scans` | number |  |
| `spice_migration_completed` | boolean |  |
| `state` | string |  |
| `tags` | array<object> |  |
| `threat_active` | boolean |  |
| `updated` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /qrcodes/:qrCodeId/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code.md) for the provider-specific parameters and requirements.

