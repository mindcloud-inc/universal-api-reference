# 5pm Universal API Examples

These examples use the MindCloud API key and 5pm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Statuses

Retrieves project statuses from 5pm.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-statuses?${params}`, {
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
      "data": {
        "item": [
          {
            "alias": {
              "_cdata": "string"
            },
            "id": "string",
            "is_final": "string",
            "name": {
              "_cdata": "Ava Chen"
            }
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [List Statuses action reference](actions/list-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pm/latest/actions/list-statuses).

## Attach Files

Uploads files to an activity in 5pm.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pm/latest/actions/attach-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pm/latest/actions/attach-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string"
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
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Attach Files action reference](actions/attach-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pm/latest/actions/attach-files).
