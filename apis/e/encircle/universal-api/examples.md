# Encircle Universal API Examples

These examples use the MindCloud API key and Encircle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Find Claim Assignments

Retrieves claim assignments from Encircle.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-assignments?connectionId=$CONNECTION_ID&propertyClaimId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyClaimId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-claim-assignments?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Find Claim Assignments action reference](actions/find-claim-assignments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encircle/latest/actions/find-claim-assignments).

## Assign User To Claim

Assigns a user to a property claim in Encircle.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/assign-user-to-claim" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyClaimId": 1,
  "userEmailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encircle/latest/actions/assign-user-to-claim', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyClaimId": 1,
    "userEmailAddress": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Assign User To Claim action reference](actions/assign-user-to-claim.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encircle/latest/actions/assign-user-to-claim).
