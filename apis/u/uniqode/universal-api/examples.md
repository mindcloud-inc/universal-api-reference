# Uniqode Universal API Examples

These examples use the MindCloud API key and Uniqode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from your Uniqode account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-organizations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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
          "allow_analytics_export": true,
          "check_response_limits": true,
          "created": "2026-05-07T12:00:00.000Z",
          "email_wallet_pass": true,
          "enforce_qr_templates": true,
          "form_service": 1,
          "id": 1,
          "name": "Ava Chen",
          "physical_web_active": true,
          "reseller_access": true,
          "updated": "2026-05-07T12:00:00.000Z",
          "wallet_active": true,
          "whitelabel_access": true
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uniqode/latest/actions/list-organizations).

## Activate QR Code

Activates a dynamic QR code in Uniqode.

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

Example response:

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

See the full [Activate QR Code action reference](actions/activate-qr-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uniqode/latest/actions/activate-qr-code).
