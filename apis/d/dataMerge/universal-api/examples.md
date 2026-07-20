# DataMerge Universal API Examples

These examples use the MindCloud API key and DataMerge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits Balance

Retrieves your current credit balance from DataMerge.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-credits-balance?${params}`, {
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

See the full [Get Credits Balance action reference](actions/get-credits-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataMerge/latest/actions/get-credits-balance).

## Add Items to List

Adds companies or contacts to a DataMerge list.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/add-items-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectType": "string",
  "list": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/add-items-to-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectType": "string",
    "list": "string"
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

See the full [Add Items to List action reference](actions/add-items-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataMerge/latest/actions/add-items-to-list).
