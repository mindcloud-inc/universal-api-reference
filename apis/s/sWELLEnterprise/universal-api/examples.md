# SWELLEnterprise Universal API Examples

These examples use the MindCloud API key and SWELLEnterprise connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Portal Configuration

Retrieves portal configuration from SWELLEnterprise.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-configuration?${params}`, {
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
      "data": {
        "allowFileSharing": true,
        "enabledModules": [
          "string"
        ],
        "isActive": true,
        "portalLogo": {},
        "portalName": "Ava Chen",
        "primaryColor": "string",
        "secondaryColor": "string",
        "showActivityFeed": true,
        "tokenExpirationDays": 1,
        "welcomeMessage": {}
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Portal Configuration action reference](actions/get-portal-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sWELLEnterprise/latest/actions/get-portal-configuration).

## Approve Project Approval

Approves a project approval in SWELLEnterprise.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/approve-project-approval" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "approvalId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/approve-project-approval', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "approvalId": 1
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
      "approved_at": "2026-05-07T12:00:00.000Z",
      "approver_user_id": 1,
      "approver": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "comments": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "project_id": 1,
      "rejected_at": "2026-05-07T12:00:00.000Z",
      "requested_by_user_id": 1,
      "requested_by": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "status": "string",
      "tenant_id": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Approve Project Approval action reference](actions/approve-project-approval.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sWELLEnterprise/latest/actions/approve-project-approval).
