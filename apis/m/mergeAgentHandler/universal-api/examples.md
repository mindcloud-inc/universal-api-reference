# Merge Agent Handler Universal API Examples

These examples use the MindCloud API key and Merge Agent Handler connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tool Packs

Retrieves tool packs from Merge Agent Handler.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/list-tool-packs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/list-tool-packs?${params}`, {
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

See the full [List Tool Packs action reference](actions/list-tool-packs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mergeAgentHandler/latest/actions/list-tool-packs).

## Bulk Upsert Connector Tool Description Overrides

Upserts or deletes connector tool description overrides in Merge Agent Handler.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/bulk-upsert-connector-tool-description-overrides" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/bulk-upsert-connector-tool-description-overrides', {
  method: 'PUT',
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

See the full [Bulk Upsert Connector Tool Description Overrides action reference](actions/bulk-upsert-connector-tool-description-overrides.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mergeAgentHandler/latest/actions/bulk-upsert-connector-tool-description-overrides).
