# DecisionVault Universal API Examples

These examples use the MindCloud API key and DecisionVault connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Matters

Retrieves matters from your firm in DecisionVault.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-matters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-matters?${params}`, {
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
      "client_type": "string",
      "close_date": "2026-05-07T12:00:00.000Z",
      "contact_main_full_name": "Ava Chen",
      "contact_main_marital_status": "string",
      "contact_main_status": "string",
      "contact_spouse_full_name": "Ava Chen",
      "id": "string",
      "is_submitted": true,
      "name": "Ava Chen",
      "open_date": "2026-05-07T12:00:00.000Z",
      "quest_approach": "string",
      "quest_internal_type": "string",
      "representative_full_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Matters action reference](actions/list-matters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/decisionVault/latest/actions/list-matters).

## Create Matter

Creates a matter in DecisionVault and returns an invite link.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/create-matter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "matterName": "Ava Chen",
  "questionnaireId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/create-matter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "matterName": "Ava Chen",
    "questionnaireId": "string"
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
      "invite_key": "string",
      "invite_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Matter action reference](actions/create-matter.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/decisionVault/latest/actions/create-matter).
