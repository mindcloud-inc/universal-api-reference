# Blip Universal API Examples

These examples use the MindCloud API key and Blip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from Blip.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blip/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blip/latest/actions/get-account?${params}`, {
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
      "from": "string",
      "id": "string",
      "metadata": {},
      "method": "string",
      "resource": {},
      "status": "string",
      "to": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blip/latest/actions/get-account).

## Add Contact

Creates a new contact in Blip.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blip/latest/actions/add-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uri": "/contacts/test.user@0mn.io",
  "resource": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blip/latest/actions/add-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uri": "/contacts/test.user@0mn.io",
    "resource": {}
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
      "from": "string",
      "id": "string",
      "metadata": {},
      "method": "string",
      "resource": {},
      "status": "string",
      "to": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact action reference](actions/add-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blip/latest/actions/add-contact).
