# WhatsBoost Universal API Examples

These examples use the MindCloud API key and WhatsBoost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Devices

Retrieves devices from WhatsBoost.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/get-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/get-devices?${params}`, {
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
      "data": [
        {}
      ],
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Devices action reference](actions/get-devices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatsBoost/latest/actions/get-devices).

## Create Contact

Creates a new contact in WhatsBoost.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string",
  "name": "Ava Chen",
  "groups": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string",
    "name": "Ava Chen",
    "groups": "string"
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
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatsBoost/latest/actions/create-contact).
