# Zeplin Universal API Examples

These examples use the MindCloud API key and Zeplin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves a list of projects from Zeplin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-projects?${params}`, {
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
      "created": 1,
      "description": "string",
      "id": "string",
      "linked_styleguide": {},
      "name": "Ava Chen",
      "number_of_colors": 1,
      "number_of_components": 1,
      "number_of_connected_components": 1,
      "number_of_members": 1,
      "number_of_screens": 1,
      "number_of_text_styles": 1,
      "platform": "string",
      "scene_url": "https://example.com",
      "status": "string",
      "thumbnail": "string",
      "updated": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zeplin/latest/actions/list-projects).

## Create Organization Webhook

Creates a new organization webhook in Zeplin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-organization-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "url": "https://example.com",
  "name": "Ava Chen",
  "secret": "string",
  "status": {},
  "projectIds[]": [
    "string"
  ],
  "styleguideIds[]": [
    "string"
  ],
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-organization-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "url": "https://example.com",
    "name": "Ava Chen",
    "secret": "string",
    "status": {},
    "projectIds[]": ["string"],
    "styleguideIds[]": ["string"],
    "events[]": ["string"]
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Organization Webhook action reference](actions/create-organization-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zeplin/latest/actions/create-organization-webhook).
