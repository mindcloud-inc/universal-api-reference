# Rocketadmin Universal API Examples

These examples use the MindCloud API key and Rocketadmin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/check-api-key?${params}`, {
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
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Check API Key action reference](actions/check-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rocketadmin/latest/actions/check-api-key).

## Add Table Row



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/add-table-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string",
  "tableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/add-table-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "string",
    "tableName": "Ava Chen"
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
      "completed": true,
      "course_id": {
        "id": "string",
        "title": "string"
      },
      "enrolled_at": "string",
      "id": "string",
      "progress": "string",
      "user_id": {
        "full_name": "Ava Chen",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Table Row action reference](actions/add-table-row.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rocketadmin/latest/actions/add-table-row).
