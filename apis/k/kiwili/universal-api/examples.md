# Kiwili Universal API Examples

These examples use the MindCloud API key and Kiwili connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Enterprises

Retrieves all enterprise records from Kiwili.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/list-enterprises?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/list-enterprises?${params}`, {
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
      "List": [
        {}
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Enterprises action reference](actions/list-enterprises.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiwili/latest/actions/list-enterprises).

## Create Contact

Creates a new contact in Kiwili.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "EnterpriseId": 1,
  "FirstName": "Ava",
  "LastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "EnterpriseId": 1,
    "FirstName": "Ava",
    "LastName": "Chen"
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
      "Email": "ava@example.com",
      "EnterpriseId": 1,
      "FirstName": "Ava",
      "Id": 1,
      "IsActive": true,
      "LastName": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiwili/latest/actions/create-contact).
