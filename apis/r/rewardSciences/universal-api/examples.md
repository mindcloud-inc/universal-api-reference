# Reward Sciences Universal API Examples

These examples use the MindCloud API key and Reward Sciences connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Reward Categories



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/list-reward-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/list-reward-categories?${params}`, {
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
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [List Reward Categories action reference](actions/list-reward-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rewardSciences/latest/actions/list-reward-categories).

## Assign External Identity To User



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/assign-external-identity-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "idp": "string",
  "identity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/assign-external-identity-to-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "idp": "string",
    "identity": "string"
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

See the full [Assign External Identity To User action reference](actions/assign-external-identity-to-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rewardSciences/latest/actions/assign-external-identity-to-user).
