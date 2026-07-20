# Testlify Universal API Examples

These examples use the MindCloud API key and Testlify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assessments

Retrieves assessments from Testlify with optional filters and pagination.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-assessments?${params}`, {
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
      "assessmentId": "string",
      "assessmentStatus": "string",
      "assessmentTitle": "string",
      "created": "string",
      "createdBy": "string",
      "groupName": "Ava Chen",
      "isArchived": true,
      "jobRoleId": "string",
      "publicInviteLink": "https://example.com",
      "totalCandidateCount": 1,
      "totalCompleted": 1,
      "totalInProgress": 1,
      "totalInvited": 1,
      "totalRejected": 1,
      "userId": "string",
      "workspaceLabel": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Assessments action reference](actions/list-assessments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testlify/latest/actions/list-assessments).

## Create Access Token

Creates a new access token in Testlify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testlify/latest/actions/create-access-token', {
  method: 'POST',
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
      "accessToken": "string",
      "created": "string",
      "createdBy": "string",
      "expiration": "string",
      "id": "string",
      "modified": "string",
      "note": "string",
      "orgId": "string",
      "status": "string",
      "userIdentifierId": "string",
      "userWorkspaceProfileId": "string",
      "workspaceUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Access Token action reference](actions/create-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testlify/latest/actions/create-access-token).
