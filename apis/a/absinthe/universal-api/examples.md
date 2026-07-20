# Absinthe Universal API Examples

These examples use the MindCloud API key and Absinthe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Campaigns

Retrieves campaigns for your Absinthe organization.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/list-campaigns?${params}`, {
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

See the full [List Campaigns action reference](actions/list-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/absinthe/latest/actions/list-campaigns).

## Claim Badge

Claims a badge for a user in Absinthe.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/claim-badge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/claim-badge', {
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

See the full [Claim Badge action reference](actions/claim-badge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/absinthe/latest/actions/claim-badge).
