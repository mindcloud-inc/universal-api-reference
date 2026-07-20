# ClustDoc Universal API Examples

These examples use the MindCloud API key and ClustDoc connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-teams?${params}`, {
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
      "cname_domain": "Ava Chen",
      "cname_status": 1,
      "id": 1,
      "name": "Ava Chen",
      "photo_url": "https://example.com",
      "user_current_team": true
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clustDoc/latest/actions/list-teams).

## Create Application



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact.email": "ava@example.com",
  "contact.firstname": "Codex",
  "contact.lastname": "Dossier",
  "template_id": "373355"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact.email": "ava@example.com",
    "contact.firstname": "Codex",
    "contact.lastname": "Dossier",
    "template_id": "373355"
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
      "contact": {},
      "count_eligible_items": 1,
      "count_missing_items": 1,
      "created_at": "string",
      "dossier_items": [
        {}
      ],
      "form_fields": [
        {}
      ],
      "id": 1,
      "is_late": true,
      "progress_percentage": 1,
      "public_url": "https://example.com",
      "secured_list_url": "https://example.com",
      "stakeholders": [
        {}
      ],
      "status": "string",
      "status_color": "string",
      "status_string": "string",
      "status_string_full": "string",
      "team": {},
      "template": {},
      "template_id": 1,
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Application action reference](actions/create-application.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clustDoc/latest/actions/create-application).
