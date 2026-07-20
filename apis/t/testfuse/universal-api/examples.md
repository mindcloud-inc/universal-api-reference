# Testfuse Universal API Examples

These examples use the MindCloud API key and Testfuse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assessment Specs

Retrieves assessment specs available in Testfuse.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessment-specs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/list-assessment-specs?${params}`, {
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
      "count": 1,
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Assessment Specs action reference](actions/list-assessment-specs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testfuse/latest/actions/list-assessment-specs).

## Invite Candidates

Invites candidates to a Testfuse assessment spec.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/invite-candidates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ],
  "specId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/invite-candidates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"],
    "specId": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Invite Candidates action reference](actions/invite-candidates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testfuse/latest/actions/invite-candidates).
