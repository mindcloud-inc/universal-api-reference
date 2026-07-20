# LinkupAPI Universal API Examples

These examples use the MindCloud API key and LinkupAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits Balance

Retrieves your current credits balance from LinkupAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/get-credits-balance?${params}`, {
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
      "balance": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits Balance action reference](actions/get-credits-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkupAPI/latest/actions/get-credits-balance).

## Create Research Task

Creates a new research task in LinkupAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/create-research-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "q": "string",
  "outputType": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/create-research-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "q": "string",
    "outputType": "0"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Research Task action reference](actions/create-research-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkupAPI/latest/actions/create-research-task).
