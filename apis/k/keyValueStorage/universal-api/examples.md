# Key Value Storage Universal API Examples

These examples use the MindCloud API key and Key Value Storage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Value



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/get-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/get-value?${params}`, {
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

See the full [Get Value action reference](actions/get-value.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keyValueStorage/latest/actions/get-value).

## Set Value



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/set-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/set-value', {
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

See the full [Set Value action reference](actions/set-value.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keyValueStorage/latest/actions/set-value).
