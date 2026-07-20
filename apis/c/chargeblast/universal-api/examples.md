# Chargeblast Universal API Examples

These examples use the MindCloud API key and Chargeblast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Alerts

Retrieves alerts from Chargeblast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-alerts?${params}`, {
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
      "alerts": [
        {}
      ],
      "page": 1,
      "per": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Fetch Alerts action reference](actions/fetch-alerts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeblast/latest/actions/fetch-alerts).

## Upload IP Data

Uploads IP data to Chargeblast.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-ip-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "ip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/upload-ip-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "ip": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Upload IP Data action reference](actions/upload-ip-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeblast/latest/actions/upload-ip-data).
