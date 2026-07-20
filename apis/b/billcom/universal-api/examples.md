# BILL Payables & Receivables Universal API Examples

These examples use the MindCloud API key and BILL Payables & Receivables connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Bill.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-users?${params}`, {
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
      "createdTime": "string",
      "email": "ava@example.com",
      "entity": "string",
      "firstName": "Ava",
      "id": "string",
      "isActive": "string",
      "isVeridVerified": true,
      "lastName": "Chen",
      "loginId": "string",
      "organizationName": "Ava Chen",
      "orgId": "string",
      "partnerUserGroupType": "string",
      "profileId": "string",
      "timezoneId": "string",
      "updatedTime": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billcom/latest/actions/list-users).

## Approve Bill

Approves a bill in Bill.com.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/approve-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billcom/latest/actions/approve-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectId": "string"
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

See the full [Approve Bill action reference](actions/approve-bill.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billcom/latest/actions/approve-bill).
