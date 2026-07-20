# Agendor Universal API Examples

These examples use the MindCloud API key and Agendor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the authenticated user from Agendor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agendor/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agendor/latest/actions/get-current-user?${params}`, {
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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agendor/latest/actions/get-current-user).

## Create Deal For Organization

Creates a new deal for an organization in Agendor.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agendor/latest/actions/create-deal-for-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deal": "string",
  "organization_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agendor/latest/actions/create-deal-for-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deal": "string",
    "organization_id": 1
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

See the full [Create Deal For Organization action reference](actions/create-deal-for-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agendor/latest/actions/create-deal-for-organization).
