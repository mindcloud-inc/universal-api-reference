# Tidely Universal API Examples

These examples use the MindCloud API key and Tidely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Connection



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidely/latest/actions/check-connection?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Check Connection action reference](actions/check-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tidely/latest/actions/check-connection).

## Add To Existing Period Plan



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/add-to-existing-period-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidely/latest/actions/add-to-existing-period-plan', {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add To Existing Period Plan action reference](actions/add-to-existing-period-plan.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tidely/latest/actions/add-to-existing-period-plan).
