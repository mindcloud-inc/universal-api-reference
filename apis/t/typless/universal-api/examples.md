# Typless Universal API Examples

These examples use the MindCloud API key and Typless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Awaiting Poll Extractions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typless/latest/actions/list-awaiting-poll-extractions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typless/latest/actions/list-awaiting-poll-extractions?${params}`, {
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
      "extraction_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Awaiting Poll Extractions action reference](actions/list-awaiting-poll-extractions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typless/latest/actions/list-awaiting-poll-extractions).

## Add Document



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "learning_fields": {},
  "file_name": "Ava Chen",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typless/latest/actions/add-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "learning_fields": {},
    "file_name": "Ava Chen",
    "file": "string"
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
      "details": [
        "string"
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Document action reference](actions/add-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typless/latest/actions/add-document).
