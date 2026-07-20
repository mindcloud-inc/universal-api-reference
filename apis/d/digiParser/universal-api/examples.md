# DigiParser Universal API Examples

These examples use the MindCloud API key and DigiParser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Parsers



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/list-parsers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/list-parsers?${params}`, {
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

See the full [List Parsers action reference](actions/list-parsers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digiParser/latest/actions/list-parsers).

## Reprocess Document



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/reprocess-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parserId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/reprocess-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parserId": "string"
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
      "documentId": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Reprocess Document action reference](actions/reprocess-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digiParser/latest/actions/reprocess-document).
