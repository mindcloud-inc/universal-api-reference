# Satiurn Universal API Examples

These examples use the MindCloud API key and Satiurn connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Labels

Retrieves labels from Satiurn.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/get-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/get-labels?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Labels action reference](actions/get-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/satiurn/latest/actions/get-labels).

## Create Board

Creates a new board in Satiurn.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/create-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/create-board', {
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

See the full [Create Board action reference](actions/create-board.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/satiurn/latest/actions/create-board).
