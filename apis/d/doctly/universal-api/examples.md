# Doctly Universal API Examples

These examples use the MindCloud API key and Doctly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Extractors



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-extractors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-extractors?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Extractors action reference](actions/list-extractors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/doctly/latest/actions/list-extractors).

## Process Document



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/process-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doctly/latest/actions/process-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "accuracy": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "id": "string",
      "pageCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Process Document action reference](actions/process-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/doctly/latest/actions/process-document).
