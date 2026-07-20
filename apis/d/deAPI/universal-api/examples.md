# deAPI Universal API Examples

These examples use the MindCloud API key and deAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Balance

Retrieves your current account balance from deAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-current-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-current-balance?${params}`, {
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

See the full [Get Current Balance action reference](actions/get-current-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deAPI/latest/actions/get-current-balance).

## Create Text-to-Embedding Job

Creates a text-to-embedding job in deAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-embedding-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-embedding-job', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Text-to-Embedding Job action reference](actions/create-text-to-embedding-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deAPI/latest/actions/create-text-to-embedding-job).
