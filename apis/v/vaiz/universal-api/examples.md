# Vaiz Universal API Examples

These examples use the MindCloud API key and Vaiz connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves the authenticated user profile from Vaiz.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/get-profile?${params}`, {
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
      "profile": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vaiz/latest/actions/get-profile).

## Add Reaction

Adds a reaction to a comment in Vaiz.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/add-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/add-reaction', {
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
      "reactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Reaction action reference](actions/add-reaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vaiz/latest/actions/add-reaction).
