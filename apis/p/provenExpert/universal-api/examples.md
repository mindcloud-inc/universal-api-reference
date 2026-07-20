# ProvenExpert Universal API Examples

These examples use the MindCloud API key and ProvenExpert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves your profile from ProvenExpert.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-profile?${params}`, {
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
      "company": "string",
      "contact": {
        "country": "string",
        "email": "ava@example.com"
      },
      "created": 1,
      "customerId": 1,
      "email": "ava@example.com",
      "expirePlan": "string",
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "plan": "string",
      "profileUrl": "https://example.com",
      "public": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/provenExpert/latest/actions/get-profile).

## Create Invitation Link

Creates a personal survey invitation link in ProvenExpert.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.code": "VRTQ13",
  "data.email": "reviewer@example.org"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.code": "VRTQ13",
    "data.email": "reviewer@example.org"
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
      "exists": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Invitation Link action reference](actions/create-invitation-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/provenExpert/latest/actions/create-invitation-link).
