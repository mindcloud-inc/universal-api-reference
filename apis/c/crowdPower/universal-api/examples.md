# CrowdPower Universal API Examples

These examples use the MindCloud API key and CrowdPower connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project

Retrieves a project from CrowdPower.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-project?${params}`, {
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
      "charges_count": 1,
      "charges_sum": 1,
      "company": {},
      "company_id": "string",
      "created_at": 1,
      "currency": "string",
      "customers_count": 1,
      "events": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "onboarded": true,
      "segments": [
        {}
      ],
      "slug": "string",
      "smtp_config": {},
      "tags": [
        {}
      ],
      "theme": {},
      "traits": [
        {}
      ],
      "unsub_groups": [
        {}
      ],
      "updated_at": 1,
      "user_id": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Project action reference](actions/get-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crowdPower/latest/actions/get-project).

## Add Notes

Updates customer notes in CrowdPower.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/add-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "notes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/add-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "notes": "string"
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
      "customer_id": "string",
      "notes": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Notes action reference](actions/add-notes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crowdPower/latest/actions/add-notes).
