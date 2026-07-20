# Clicksign Universal API Examples

These examples use the MindCloud API key and Clicksign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Envelopes

Retrieves envelopes from Clicksign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/list-envelopes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/list-envelopes?${params}`, {
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

See the full [List Envelopes action reference](actions/list-envelopes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clicksign/latest/actions/list-envelopes).

## Create Authentication Requirement

Creates an authentication requirement in Clicksign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-authentication-requirement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.auth": "string",
  "data.relationships.document.data.id": "string",
  "data.relationships.signer.data.id": "string",
  "envelopeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-authentication-requirement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.auth": "string",
    "data.relationships.document.data.id": "string",
    "data.relationships.signer.data.id": "string",
    "envelopeId": "string"
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

See the full [Create Authentication Requirement action reference](actions/create-authentication-requirement.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clicksign/latest/actions/create-authentication-requirement).
