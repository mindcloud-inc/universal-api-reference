# Chargback Universal API Examples

These examples use the MindCloud API key and Chargback connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Business Accounts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-business-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-business-accounts?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Business Accounts action reference](actions/list-business-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargback/latest/actions/list-business-accounts).

## Change Alert Status

Updates an existing alert status in Chargback.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/change-alert-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "external_id": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargback/latest/actions/change-alert-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "external_id": "string",
    "status": "string"
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
      "alert_id": "string",
      "message": "string",
      "new_status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Change Alert Status action reference](actions/change-alert-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargback/latest/actions/change-alert-status).
