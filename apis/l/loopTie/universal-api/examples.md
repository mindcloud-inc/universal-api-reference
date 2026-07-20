# Loop & Tie Universal API Examples

These examples use the MindCloud API key and Loop & Tie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams available in Loop & Tie.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/list-teams?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopTie/latest/actions/list-teams).

## Bulk Create Gifts

Creates multiple gifts at once in Loop & Tie.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/bulk-create-gifts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/bulk-create-gifts', {
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
      "data": [
        {}
      ],
      "included": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create Gifts action reference](actions/bulk-create-gifts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopTie/latest/actions/bulk-create-gifts).
