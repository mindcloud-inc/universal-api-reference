# redirect.pizza Universal API Examples

These examples use the MindCloud API key and redirect.pizza connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Team Details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-team-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-team-details?${params}`, {
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
      "hits": {},
      "hostnames": {},
      "id": 1,
      "name": "Ava Chen",
      "users": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Team Details action reference](actions/get-team-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/redirectpizza/latest/actions/get-team-details).

## Apply Automatic DNS



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/apply-automatic-dns" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/apply-automatic-dns', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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
      "output": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

See the full [Apply Automatic DNS action reference](actions/apply-automatic-dns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/redirectpizza/latest/actions/apply-automatic-dns).
