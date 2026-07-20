# SeekTable Universal API Examples

These examples use the MindCloud API key and SeekTable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Reports

Retrieves saved reports from your SeekTable account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/list-reports?${params}`, {
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
      "canEdit": true,
      "canShareToTeam": true,
      "config": "string",
      "createDate": "string",
      "cubeId": "string",
      "id": "string",
      "isPublic": true,
      "isSubscribed": true,
      "name": "Ava Chen",
      "reportType": "string",
      "shared": true,
      "updateDate": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Reports action reference](actions/list-reports.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seekTable/latest/actions/list-reports).

## Add Team Members

Adds team members to a SeekTable account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/add-team-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/add-team-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "emails[]": ["ava@example.com"]
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

See the full [Add Team Members action reference](actions/add-team-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seekTable/latest/actions/add-team-members).
