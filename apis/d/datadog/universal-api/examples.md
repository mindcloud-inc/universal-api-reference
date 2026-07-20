# Datadog Universal API Examples

These examples use the MindCloud API key and Datadog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Monitors

Retrieves monitors from Datadog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-monitors?${params}`, {
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
      "created": "string",
      "creator": {},
      "draft_status": "string",
      "id": 1,
      "message": "string",
      "modified": "string",
      "name": "Ava Chen",
      "options": {},
      "org_id": 1,
      "overall_state": "string",
      "priority": 1,
      "query": "string",
      "restricted_roles": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Monitors action reference](actions/list-monitors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datadog/latest/actions/list-monitors).

## Create Dashboard

Creates a new dashboard in Datadog.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "layoutType": "string",
  "widgets[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-dashboard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "layoutType": "string",
    "widgets[]": [{}]
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
      "authorHandle": "string",
      "authorName": "Ava Chen",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "isReadOnly": true,
      "layoutType": "string",
      "modifiedAt": "string",
      "notifyList": [
        "string"
      ],
      "reflowType": "string",
      "restrictedRoles": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "templateVariablePresets": [
        {}
      ],
      "templateVariables": [
        {}
      ],
      "title": "string",
      "url": "https://example.com",
      "widgets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Dashboard action reference](actions/create-dashboard.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datadog/latest/actions/create-dashboard).
