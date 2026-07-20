# HeyPoplar Universal API Examples

These examples use the MindCloud API key and HeyPoplar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Organization

Retrieves the current organization from HeyPoplar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-current-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-current-organization?${params}`, {
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
      "mode": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Organization action reference](actions/get-current-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/heyPoplar/latest/actions/get-current-organization).

## Add Do Not Mail Entry

Creates a do-not-mail entry in HeyPoplar.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/add-do-not-mail-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/add-do-not-mail-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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

See the full [Add Do Not Mail Entry action reference](actions/add-do-not-mail-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/heyPoplar/latest/actions/add-do-not-mail-entry).
