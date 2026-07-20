# Uniqode: List QR Codes

Retrieves QR codes from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-qr-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-qr-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-qr-codes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
          "threat_active": true,
          "updated": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |
| `results[].campaign` | object |  |
| `results[].campaign.campaign_active` | boolean |  |
| `results[].campaign.content_type` | number |  |
| `results[].campaign.created` | date |  |
| `results[].campaign.custom_url` | string |  |
| `results[].campaign.id` | number |  |
| `results[].campaign.name` | string |  |
| `results[].campaign.updated` | date |  |
| `results[].created` | date |  |
| `results[].creation_source` | string |  |
| `results[].domain` | number |  |
| `results[].id` | number |  |
| `results[].location_enabled` | boolean |  |
| `results[].maintainer` | number |  |
| `results[].name` | string |  |
| `results[].notes` | string |  |
| `results[].organization` | number |  |
| `results[].qr_type` | number |  |
| `results[].scans` | number |  |
| `results[].spice_migration_completed` | boolean |  |
| `results[].state` | string |  |
| `results[].threat_active` | boolean |  |
| `results[].updated` | date |  |
| `results[].url` | string |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /qrcodes/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-qr-codes.md) for the provider-specific parameters and requirements.

