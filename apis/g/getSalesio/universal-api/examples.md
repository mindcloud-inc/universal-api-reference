# GetSales.io Universal API Examples

These examples use the MindCloud API key and GetSales.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-lists?${params}`, {
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
      "name": "Ava Chen",
      "team_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/getSalesio/latest/actions/list-lists).

## Add Contact To Automation



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-contact-to-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flowUuid": "string",
  "leadUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-contact-to-automation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flowUuid": "string",
    "leadUuid": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact To Automation action reference](actions/add-contact-to-automation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/getSalesio/latest/actions/add-contact-to-automation).
