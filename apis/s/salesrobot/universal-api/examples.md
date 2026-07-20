# Salesrobot Universal API Examples

These examples use the MindCloud API key and Salesrobot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List LinkedIn Accounts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/list-linked-in-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/list-linked-in-accounts?${params}`, {
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

See the full [List LinkedIn Accounts action reference](actions/list-linked-in-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesrobot/latest/actions/list-linked-in-accounts).

## Add Campaign Sequence Steps



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/add-campaign-sequence-steps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/add-campaign-sequence-steps', {
  method: 'PUT',
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

See the full [Add Campaign Sequence Steps action reference](actions/add-campaign-sequence-steps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesrobot/latest/actions/add-campaign-sequence-steps).
