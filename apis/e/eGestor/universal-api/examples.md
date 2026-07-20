# eGestor Universal API Examples

These examples use the MindCloud API key and eGestor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Pix Status

Retrieves the status of a Pix charge from eGestor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/check-pix-status?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/check-pix-status?${params}`, {
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

See the full [Check Pix Status action reference](actions/check-pix-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eGestor/latest/actions/check-pix-status).

## Create Contact

Creates a new contact in eGestor.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nome": "Kaya Labadie",
  "tipo[]": "cliente"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nome": "Kaya Labadie",
    "tipo[]": "cliente"
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
      "codigo": 1,
      "nome": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eGestor/latest/actions/create-contact).
