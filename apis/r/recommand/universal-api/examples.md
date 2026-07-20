# Recommand Universal API Examples

These examples use the MindCloud API key and Recommand connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Authentication

Validates the current Recommand API credentials.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-authentication?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Verify Authentication action reference](actions/verify-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recommand/latest/actions/verify-authentication).

## Assign Label to Document

Assigns a label to a Recommand document.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/assign-label-to-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentid": "string",
  "labelid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/assign-label-to-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentid": "string",
    "labelid": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Assign Label to Document action reference](actions/assign-label-to-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recommand/latest/actions/assign-label-to-document).
