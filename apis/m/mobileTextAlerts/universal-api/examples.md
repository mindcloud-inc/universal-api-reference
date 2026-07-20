# Mobile Text Alerts Universal API Examples

These examples use the MindCloud API key and Mobile Text Alerts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify API Key

Retrieves API key verification details from Mobile Text Alerts.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/verify-api-key?${params}`, {
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify API Key action reference](actions/verify-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mobileTextAlerts/latest/actions/verify-api-key).

## Create Subscriber

Creates a new subscriber in Mobile Text Alerts.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/create-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/create-subscriber', {
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Subscriber action reference](actions/create-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mobileTextAlerts/latest/actions/create-subscriber).
