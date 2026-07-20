# SARE Universal API Examples

These examples use the MindCloud API key and SARE connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available Group Numbers

Lists available group numbers in SARE.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-available-group-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-available-group-numbers?${params}`, {
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
      "code": 1,
      "response": [
        1
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Available Group Numbers action reference](actions/list-available-group-numbers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sARE/latest/actions/list-available-group-numbers).

## Add Subscribers

Creates new subscribers in SARE.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/add-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sARE/latest/actions/add-subscribers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": [{}]
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

See the full [Add Subscribers action reference](actions/add-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sARE/latest/actions/add-subscribers).
