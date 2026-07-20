# Sapling Universal API Examples

These examples use the MindCloud API key and Sapling connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Dictionary Entries

Retrieves custom dictionary entries from Sapling.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-dictionary-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-dictionary-entries?${params}`, {
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
      "created_at": "string",
      "entry": "string",
      "id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Dictionary Entries action reference](actions/list-dictionary-entries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sapling/latest/actions/list-dictionary-entries).

## Accept Completion

Records an accepted autocomplete completion in Sapling.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/accept-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "completionId": "string",
  "query": "string",
  "completion": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sapling/latest/actions/accept-completion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "completionId": "string",
    "query": "string",
    "completion": "string"
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Accept Completion action reference](actions/accept-completion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sapling/latest/actions/accept-completion).
