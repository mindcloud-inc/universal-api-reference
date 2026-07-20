# SendSafely Universal API Examples

These examples use the MindCloud API key and SendSafely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Credentials



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/verify-credentials?${params}`, {
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
      "message": "string",
      "requiresApprover": true,
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Credentials action reference](actions/verify-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendSafely/latest/actions/verify-credentials).

## Add Contact Group Member



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/add-contact-group-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/add-contact-group-member', {
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
  "data": [
    {
      "response": "string",
      "userEmail": "ava@example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Group Member action reference](actions/add-contact-group-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendSafely/latest/actions/add-contact-group-member).
