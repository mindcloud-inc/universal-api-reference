# CompanyHub Universal API Examples

These examples use the MindCloud API key and CompanyHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from CompanyHub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/get-current-user?${params}`, {
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
      "emailAddress": "ava@example.com",
      "isSandbox": true,
      "name": "Ava Chen",
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/companyHub/latest/actions/get-current-user).

## Create Record

Creates a new record in a CompanyHub table.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableName": "Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableName": "Contact"
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
      "id": 1,
      "isDuplicate": true,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Record action reference](actions/create-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/companyHub/latest/actions/create-record).
