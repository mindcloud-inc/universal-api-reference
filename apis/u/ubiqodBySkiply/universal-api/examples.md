# Ubiqod by Skiply Universal API Examples

These examples use the MindCloud API key and Ubiqod by Skiply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Badge Lists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-badge-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-badge-lists?${params}`, {
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
      "list": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Badge Lists action reference](actions/list-badge-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ubiqodBySkiply/latest/actions/list-badge-lists).

## Add Badges To Badge List



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-badges-to-badge-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "badgeListId": "string",
  "list[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-badges-to-badge-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "badgeListId": "string",
    "list[]": [{}]
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
      "id": "string",
      "label": "string",
      "list": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Badges To Badge List action reference](actions/add-badges-to-badge-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ubiqodBySkiply/latest/actions/add-badges-to-badge-list).
