# LinkedCamp Universal API Examples

These examples use the MindCloud API key and LinkedCamp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account API Token



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-account-api-token?connectionId=$CONNECTION_ID&accountEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-account-api-token?${params}`, {
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
      "message": "string",
      "success": true,
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account API Token action reference](actions/get-account-api-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkedCamp/latest/actions/get-account-api-token).

## Add Blacklist Entry



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-blacklist-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyword": "string",
  "type": "string",
  "linkedInAccountEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-blacklist-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyword": "string",
    "type": "string",
    "linkedInAccountEmail": "ava@example.com"
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Blacklist Entry action reference](actions/add-blacklist-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkedCamp/latest/actions/add-blacklist-entry).
