# Dropcontact Universal API Examples

These examples use the MindCloud API key and Dropcontact connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits Left

Retrieves remaining credits from Dropcontact.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/get-credits-left?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/get-credits-left?${params}`, {
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
      "credits_left": 1,
      "error": true,
      "request_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Credits Left action reference](actions/get-credits-left.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropcontact/latest/actions/get-credits-left).

## Enrich Contacts

Creates a contact enrichment request in Dropcontact.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/enrich-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/enrich-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
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
      "credits_left": 1,
      "error": true,
      "request_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Enrich Contacts action reference](actions/enrich-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropcontact/latest/actions/enrich-contacts).
