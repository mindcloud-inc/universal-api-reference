# Neon Universal API Examples

These examples use the MindCloud API key and Neon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve current user details

Retrieves current user details from Neon.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-current-user-info?${params}`, {
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
      "active_seconds_limit": 1,
      "auth_accounts": [
        {}
      ],
      "billing_account": {},
      "branches_limit": 1,
      "compute_seconds_limit": 1,
      "email": "ava@example.com",
      "id": "string",
      "image": "string",
      "last_name": "Chen",
      "login": "string",
      "max_autoscaling_limit": 1,
      "name": "Ava Chen",
      "plan": "string",
      "projects_limit": 1
    }
  ],
  "meta": {}
}
```

See the full [Retrieve current user details action reference](actions/get-current-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neon/latest/actions/get-current-user-info).

## Accept a project transfer request

Accepts a project transfer request in Neon.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/accept-project-transfer-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "request_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/accept-project-transfer-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "request_id": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Accept a project transfer request action reference](actions/accept-project-transfer-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neon/latest/actions/accept-project-transfer-request).
