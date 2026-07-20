# urlscan.io Universal API Examples

These examples use the MindCloud API key and urlscan.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Quotas

Retrieves your current API quotas from urlscan.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-quotas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-quotas?${params}`, {
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
      "limits": {},
      "scope": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Quotas action reference](actions/get-quotas.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/urlscanio/latest/actions/get-quotas).

## Close Incident

Updates an incident by closing it in urlscan.io.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/close-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/close-incident', {
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
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Close Incident action reference](actions/close-incident.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/urlscanio/latest/actions/close-incident).
