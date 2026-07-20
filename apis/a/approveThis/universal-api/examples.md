# ApproveThis Universal API Examples

These examples use the MindCloud API key and ApproveThis connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workflows

Retrieves approval workflows from your ApproveThis workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-workflows?${params}`, {
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
      "completedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "templateId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Workflows action reference](actions/list-workflows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/approveThis/latest/actions/list-workflows).

## Create Template

Creates a new approval template in ApproveThis.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Quarterly Budget Request",
  "slug": "quarterly-budget-request"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Quarterly Budget Request",
    "slug": "quarterly-budget-request"
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
      "allowAnonymousResponses": true,
      "createdAt": "string",
      "description": "string",
      "id": 1,
      "isActive": true,
      "name": "Ava Chen",
      "ownerId": "string",
      "ownerType": "string",
      "settings": {
        "allowResubmissions": true,
        "commentsEnabled": true,
        "commentsImmutable": true,
        "loginForApprovers": true,
        "maxResubmissions": {},
        "signedUrlExpirationDays": 1,
        "signedUrlsEnabled": true
      },
      "slug": "string",
      "teamId": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Template action reference](actions/create-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/approveThis/latest/actions/create-template).
