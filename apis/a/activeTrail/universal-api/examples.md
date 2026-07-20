# ActiveTrail Universal API Examples

These examples use the MindCloud API key and ActiveTrail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Campaigns

Retrieves a list of campaigns from ActiveTrail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/list-campaigns?${params}`, {
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

See the full [List Campaigns action reference](actions/list-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activeTrail/latest/actions/list-campaigns).

## Add Contact to Group

Adds a contact to a group in ActiveTrail.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/add-contact-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/add-contact-to-group', {
  method: 'POST',
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
  "data": [],
  "meta": {}
}
```

See the full [Add Contact to Group action reference](actions/add-contact-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activeTrail/latest/actions/add-contact-to-group).
