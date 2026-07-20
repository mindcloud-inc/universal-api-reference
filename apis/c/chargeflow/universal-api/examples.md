# Chargeflow Universal API Examples

These examples use the MindCloud API key and Chargeflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Access Key

Verifies a Chargeflow API access key.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/verify-access-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/verify-access-key?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Access Key action reference](actions/verify-access-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeflow/latest/actions/verify-access-key).

## Create Account

Creates a new Chargeflow Connect account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "business_name": "Ava Chen",
      "business_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "ext_account_id": "string",
      "id": "string",
      "owner_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeflow/latest/actions/create-account).
