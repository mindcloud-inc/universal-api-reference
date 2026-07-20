# RollWorks Universal API Examples

These examples use the MindCloud API key and RollWorks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Advertisers

Retrieves advertisers from RollWorks.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-advertisers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-advertisers?${params}`, {
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

See the full [List Advertisers action reference](actions/list-advertisers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rollWorks/latest/actions/list-advertisers).

## Accept Segment Sharing Invitation

Accepts a segment sharing invitation in RollWorks.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/accept-segment-sharing-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/accept-segment-sharing-invitation', {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Accept Segment Sharing Invitation action reference](actions/accept-segment-sharing-invitation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rollWorks/latest/actions/accept-segment-sharing-invitation).
