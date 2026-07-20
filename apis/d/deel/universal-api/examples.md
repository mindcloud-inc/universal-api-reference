# Deel Universal API Examples

These examples use the MindCloud API key and Deel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contracts

Retrieves a paginated list of contracts from Deel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deel/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deel/latest/actions/list-contracts?${params}`, {
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

See the full [List Contracts action reference](actions/list-contracts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deel/latest/actions/list-contracts).

## Create Contract Adjustment

Creates a contract adjustment in Deel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deel/latest/actions/create-contract-adjustment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deel/latest/actions/create-contract-adjustment', {
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

See the full [Create Contract Adjustment action reference](actions/create-contract-adjustment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deel/latest/actions/create-contract-adjustment).
