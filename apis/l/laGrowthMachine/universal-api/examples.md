# LaGrowthMachine Universal API Examples

These examples use the MindCloud API key and LaGrowthMachine connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Members

Retrieves members from LaGrowthMachine.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/list-members?${params}`, {
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
      "id": "string",
      "label": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Members action reference](actions/list-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/laGrowthMachine/latest/actions/list-members).

## Create Audience from LinkedIn URL

Creates an audience in LaGrowthMachine from a LinkedIn URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-audience-from-linked-in-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audience": "string",
  "identityId": "string",
  "linkedinUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-audience-from-linked-in-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audience": "string",
    "identityId": "string",
    "linkedinUrl": "https://example.com"
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
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Audience from LinkedIn URL action reference](actions/create-audience-from-linked-in-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/laGrowthMachine/latest/actions/create-audience-from-linked-in-url).
