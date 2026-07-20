# TestDome Universal API Examples

These examples use the MindCloud API key and TestDome connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Plan

Retrieves the current plan from TestDome.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-current-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-current-plan?${params}`, {
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
      "_links": {},
      "canCloneQuestions": {},
      "canCreateTest": {},
      "id": 1,
      "isPaymentSubscriptionActive": true,
      "isSubscription": true,
      "isTrial": true,
      "name": "Ava Chen",
      "questionsToCloneAvailable": 1,
      "supportsPremiumFeatures": {},
      "supportsSso": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Plan action reference](actions/get-current-plan.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testDome/latest/actions/get-current-plan).

## Archive Candidates

Archives candidates in TestDome.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/archive-candidates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "candidateIds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/archive-candidates', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "candidateIds": 1
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
      "_links": {},
      "failedCandidates": [
        1
      ]
    }
  ],
  "meta": {}
}
```

See the full [Archive Candidates action reference](actions/archive-candidates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testDome/latest/actions/archive-candidates).
