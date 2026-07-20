# Cursion Universal API Examples

These examples use the MindCloud API key and Cursion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites

Retrieves a list of sites from Cursion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/list-sites?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cursion/latest/actions/list-sites).

## Create Alert



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actions": {},
  "expressions": {},
  "name": "Ava Chen",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actions": {},
    "expressions": {},
    "name": "Ava Chen",
    "siteId": "string"
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
      "account": "string",
      "actions": [
        {}
      ],
      "expressions": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "schedule": "string",
      "time_created": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Alert action reference](actions/create-alert.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cursion/latest/actions/create-alert).
