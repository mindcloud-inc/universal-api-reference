# Password Pusher Universal API Examples

These examples use the MindCloud API key and Password Pusher connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves a list of workspaces from Password Pusher.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-accounts?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passwordPusher/latest/actions/list-accounts).

## Create Push

Creates a secure push in Password Pusher.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-push" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "push.payload": "temporary onboarding password"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-push', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "push.payload": "temporary onboarding password"
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
      "account_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "days_remaining": 1,
      "deletable_by_viewer": true,
      "deleted": true,
      "expire_after_days": 1,
      "expire_after_duration": 1,
      "expire_after_views": 1,
      "expired": true,
      "expired_on": "2026-05-07T12:00:00.000Z",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "expires_in": 1,
      "html_url": "https://example.com",
      "json_url": "https://example.com",
      "name": "Ava Chen",
      "note": "string",
      "passphrase": "string",
      "retrieval_step": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url_token": "https://example.com",
      "views_remaining": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Push action reference](actions/create-push.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passwordPusher/latest/actions/create-push).
