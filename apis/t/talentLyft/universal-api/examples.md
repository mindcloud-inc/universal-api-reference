# TalentLyft Universal API Examples

These examples use the MindCloud API key and TalentLyft connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Members

Retrieves all company members from TalentLyft.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/list-members?${params}`, {
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

See the full [List Members action reference](actions/list-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talentLyft/latest/actions/list-members).

## Create Department

Creates a new department in TalentLyft.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/create-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLyft/latest/actions/create-department', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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

See the full [Create Department action reference](actions/create-department.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talentLyft/latest/actions/create-department).
