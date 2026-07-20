# JetAPI Universal API Examples

These examples use the MindCloud API key and JetAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from JetAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/get-account?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jetAPI/latest/actions/get-account).

## Create Bulk Delivery

Creates a new bulk delivery in JetAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-bulk-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "Bulk message",
  "phonesNumbers[]": "995598464533"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-bulk-delivery', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "Bulk message",
    "phonesNumbers[]": "995598464533"
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
      "dispatchRouting": [
        "string"
      ],
      "phonesNumbers": [
        "string"
      ],
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "senderName": "Ava Chen",
      "state": 1,
      "text": "string",
      "urlShorting": true,
      "utmMark": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Delivery action reference](actions/create-bulk-delivery.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jetAPI/latest/actions/create-bulk-delivery).
