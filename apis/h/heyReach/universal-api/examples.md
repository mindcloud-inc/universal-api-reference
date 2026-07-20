# Hey Reach Universal API Examples

These examples use the MindCloud API key and Hey Reach connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List LinkedIn Accounts

Retrieves LinkedIn accounts from Hey Reach.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-linked-in-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-linked-in-accounts?${params}`, {
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
      "items": [
        {}
      ],
      "totalCount": "string"
    }
  ],
  "meta": {}
}
```

See the full [List LinkedIn Accounts action reference](actions/list-linked-in-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/heyReach/latest/actions/list-linked-in-accounts).

## Add Lead Tags

Adds tags to a lead in Hey Reach.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-lead-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-lead-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags[]": ["string"]
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
      "newAssignedTags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Lead Tags action reference](actions/add-lead-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/heyReach/latest/actions/add-lead-tags).
