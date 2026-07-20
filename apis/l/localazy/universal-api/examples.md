# Localazy Universal API Examples

These examples use the MindCloud API key and Localazy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Localazy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-projects?${params}`, {
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
      "description": "string",
      "id": "string",
      "image": "string",
      "languages": [
        {}
      ],
      "name": "Ava Chen",
      "organization": {},
      "orgId": "string",
      "role": "string",
      "slug": "string",
      "sourceLanguage": 1,
      "tone": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/localazy/latest/actions/list-projects).

## Create Glossary Term

Creates a new glossary term in a Localazy project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/create-glossary-term" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "term[]": [
    {}
  ],
  "term[].lang": "string",
  "term[].term": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/localazy/latest/actions/create-glossary-term', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "term[]": [{}],
    "term[].lang": "string",
    "term[].term": "string"
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Glossary Term action reference](actions/create-glossary-term.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/localazy/latest/actions/create-glossary-term).
