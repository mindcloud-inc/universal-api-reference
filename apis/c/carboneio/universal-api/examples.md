# Carbone.io Universal API Examples

These examples use the MindCloud API key and Carbone.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves templates from Carbone.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/list-templates?${params}`, {
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
      "category": "string",
      "comment": "string",
      "createdAt": 1,
      "deployedAt": 1,
      "expireAt": 1,
      "id": "string",
      "name": "Ava Chen",
      "origin": 1,
      "size": 1,
      "tags": [
        "string"
      ],
      "type": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/carboneio/latest/actions/list-templates).

## Convert Document

Creates a converted document from uploaded templates in Carbone.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/convert-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "template": "PGh0bWw+PGJvZHk+SGVsbG8ge2QubmFtZX08L2JvZHk+PC9odG1sPg=="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/convert-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "template": "PGh0bWw+PGJvZHk+SGVsbG8ge2QubmFtZX08L2JvZHk+PC9odG1sPg=="
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
      "renderId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert Document action reference](actions/convert-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/carboneio/latest/actions/convert-document).
