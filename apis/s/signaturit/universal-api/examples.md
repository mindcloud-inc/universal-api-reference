# Signaturit Universal API Examples

These examples use the MindCloud API key and Signaturit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves account credits from Signaturit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-credits?${params}`, {
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
      "currentPeriod": {
        "from": "string",
        "to": "string"
      },
      "period": "string",
      "quantity": 1,
      "remainingCredits": 1,
      "type": "string",
      "usedCredits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signaturit/latest/actions/get-credits).

## Create Contact

Creates a new contact in Signaturit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "sandbox-contact@example.com",
  "name": "Sandbox Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "sandbox-contact@example.com",
    "name": "Sandbox Contact"
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
      "created_at": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signaturit/latest/actions/create-contact).
