# IssueBadge Universal API Examples

These examples use the MindCloud API key and IssueBadge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Badges



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/list-badges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/list-badges?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Badges action reference](actions/list-badges.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/issueBadge/latest/actions/list-badges).

## Create Badge



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/create-badge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "badge_logo": "string",
  "issuingOrganizationName": "Ava Chen",
  "idempotencyKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/create-badge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "badge_logo": "string",
    "issuingOrganizationName": "Ava Chen",
    "idempotencyKey": "string"
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
      "badgeId": "string",
      "organizationId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Badge action reference](actions/create-badge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/issueBadge/latest/actions/create-badge).
