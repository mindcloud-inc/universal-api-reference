# Atlas AI Revenue Engine Universal API Examples

These examples use the MindCloud API key and Atlas AI Revenue Engine connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Campaigns



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/list-campaigns?${params}`, {
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

See the full [List Campaigns action reference](actions/list-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atlasAIRevenueEngine/latest/actions/list-campaigns).

## Add Knowledge Base File to Collection



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/add-knowledge-base-file-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tagName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/add-knowledge-base-file-to-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tagName": "Ava Chen"
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

See the full [Add Knowledge Base File to Collection action reference](actions/add-knowledge-base-file-to-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atlasAIRevenueEngine/latest/actions/add-knowledge-base-file-to-collection).
