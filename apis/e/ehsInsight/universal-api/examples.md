# EHS Insight Universal API Examples

These examples use the MindCloud API key and EHS Insight connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Hierarchy List



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-hierarchy-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-hierarchy-list?${params}`, {
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

See the full [Get Hierarchy List action reference](actions/get-hierarchy-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ehsInsight/latest/actions/get-hierarchy-list).

## Add Entity



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/add-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityName": "Asset"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/add-entity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityName": "Asset"
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

See the full [Add Entity action reference](actions/add-entity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ehsInsight/latest/actions/add-entity).
