# NetHunt CRM Universal API Examples

These examples use the MindCloud API key and NetHunt CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Request Credentials

Verifies request credentials for NetHunt CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/verify-request-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/verify-request-credentials?${params}`, {
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
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Verify Request Credentials action reference](actions/verify-request-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netHuntCRM/latest/actions/verify-request-credentials).

## Add Gmail Thread to Record

Adds a Gmail thread to a NetHunt CRM record.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/add-gmail-thread-to-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gmailThreadId": "string",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/add-gmail-thread-to-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gmailThreadId": "string",
    "recordId": "string"
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

See the full [Add Gmail Thread to Record action reference](actions/add-gmail-thread-to-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netHuntCRM/latest/actions/add-gmail-thread-to-record).
