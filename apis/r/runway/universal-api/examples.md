# Runway Universal API Examples

These examples use the MindCloud API key and Runway connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization Information

Retrieves organization information from Runway.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-organization-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-organization-information?${params}`, {
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
      "creditBalance": 1,
      "tier": {},
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Organization Information action reference](actions/get-organization-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runway/latest/actions/get-organization-information).

## Control A Character

Creates a character performance task in Runway.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/control-a-character" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "character": {},
  "model": "act_two",
  "reference": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/control-a-character', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "character": {},
    "model": "act_two",
    "reference": {}
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
      "error": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Control A Character action reference](actions/control-a-character.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runway/latest/actions/control-a-character).
