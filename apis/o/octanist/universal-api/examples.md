# Octanist Universal API Examples

These examples use the MindCloud API key and Octanist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Key

Checks whether an Octanist API key is valid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octanist/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octanist/latest/actions/check-api-key?${params}`, {
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

See the full [Check API Key action reference](actions/check-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/octanist/latest/actions/check-api-key).

## Create Lead

Creates a new lead in Octanist.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/octanist/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/octanist/latest/actions/create-lead', {
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

See the full [Create Lead action reference](actions/create-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/octanist/latest/actions/create-lead).
