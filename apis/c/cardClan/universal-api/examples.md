# CardClan Universal API Examples

These examples use the MindCloud API key and CardClan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces accessible to the CardClan integration.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-workspaces?${params}`, {
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
      "_id": "string",
      "choices": [
        {}
      ],
      "key": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cardClan/latest/actions/list-workspaces).

## Create Integration Configuration

Creates a CardClan integration configuration for a card workflow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/create-integration-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "workspaceId": "string",
  "cardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/create-integration-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "workspaceId": "string",
    "cardId": "string"
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Integration Configuration action reference](actions/create-integration-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cardClan/latest/actions/create-integration-configuration).
