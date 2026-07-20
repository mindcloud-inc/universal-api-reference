# CallKeeper Universal API Examples

These examples use the MindCloud API key and CallKeeper connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Info

Retrieves current user information from CallKeeper.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/get-current-user-info?${params}`, {
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
      "avatar_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "email_verified": true,
      "first_name": "Ava",
      "id": "string",
      "is_active": true,
      "last_login_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "phone": "string",
      "subscription_plan": "string",
      "subscription_status": "string",
      "timezone": "string",
      "twilio_phone_number": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Info action reference](actions/get-current-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callKeeper/latest/actions/get-current-user-info).

## Add Party To Call

Updates a call in CallKeeper by adding a party.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/add-party-to-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/add-party-to-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callId": "string"
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "page": 1,
      "page_size": 1,
      "status": "string",
      "total": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Party To Call action reference](actions/add-party-to-call.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callKeeper/latest/actions/add-party-to-call).
