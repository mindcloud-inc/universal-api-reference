# Sales Cookie Universal API Examples

These examples use the MindCloud API key and Sales Cookie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calculations

Retrieves calculation records from Sales Cookie.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculations?${params}`, {
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
      "actualThresholdsXml": "string",
      "approvalType": "string",
      "autoReleaseCredits": true,
      "autoReleaseRewards": true,
      "autoReplacePrevious": true,
      "autoRun": true,
      "autoRunId": {},
      "autoRunNotAllowed": true,
      "calculationsFinished": "string",
      "calculationsStarted": "string",
      "created": "string",
      "createdById": "string",
      "creditedTargetCount": 1,
      "creditedTransactionCount": 1,
      "creditsReleased": true,
      "creditsReleasedDate": "string",
      "customProperties": {},
      "debugOutput": {},
      "endDate": "string",
      "id": "string",
      "isDeleted": true,
      "isLocked": true,
      "name": "Ava Chen",
      "nonCreditedTargetCount": 1,
      "planId": "string",
      "planName": "Ava Chen",
      "planSnapshotXml": "string",
      "reRunCalculationId": {},
      "reRunPreserveApprovals": true,
      "reRunPreserveManualResults": true,
      "resultsReleased": true,
      "resultsReleasedDate": "string",
      "resultsReleasedMainDate": "string",
      "scannedTransactionCount": 1,
      "simulatedCount": 1,
      "simulationCount": 1,
      "startDate": "string",
      "status": "string",
      "tag": "string",
      "updated": "string",
      "updatedById": "string",
      "workspaceCurrency": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Calculations action reference](actions/list-calculations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesCookie/latest/actions/list-calculations).

## Add User To Team

Adds a user to a team in Sales Cookie.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/add-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "systemUserId": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/add-user-to-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "systemUserId": "string",
    "teamId": "string"
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
      "systemUserId": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add User To Team action reference](actions/add-user-to-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesCookie/latest/actions/add-user-to-team).
