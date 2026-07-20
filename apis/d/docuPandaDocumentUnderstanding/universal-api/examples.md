# DocuPanda - Document Understanding Universal API Examples

These examples use the MindCloud API key and DocuPanda - Document Understanding connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves workspace account details from DocuPanda.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-account-information?${params}`, {
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
      "overageCredits": 1,
      "planName": "Ava Chen",
      "remainingCredits": 1,
      "renewalDate": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuPandaDocumentUnderstanding/latest/actions/get-account-information).

## Add Workspace Member

Creates a workspace member in DocuPanda.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/add-workspace-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memberEmail": "ava@example.com",
  "memberUserId": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/add-workspace-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memberEmail": "ava@example.com",
    "memberUserId": "string",
    "workspaceId": "string"
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
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Workspace Member action reference](actions/add-workspace-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuPandaDocumentUnderstanding/latest/actions/add-workspace-member).
