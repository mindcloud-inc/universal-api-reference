# SmartReach Universal API Examples

These examples use the MindCloud API key and SmartReach connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams from SmartReach.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-teams?${params}`, {
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
      "links": {
        "next": "https://example.com"
      },
      "teams": [
        {
          "id": "string",
          "status": "string",
          "team_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartReach/latest/actions/list-teams).

## Add Domains to Do Not Contact List

Adds domains to the do not contact list in SmartReach.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-domains-to-do-not-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-domains-to-do-not-contact-list', {
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
  "data": [
    {
      "do_not_contacts": [
        {
          "do_not_contact_type": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Domains to Do Not Contact List action reference](actions/add-domains-to-do-not-contact-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartReach/latest/actions/add-domains-to-do-not-contact-list).
