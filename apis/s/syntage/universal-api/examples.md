# Syntage Universal API Examples

These examples use the MindCloud API key and Syntage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Entities

Retrieves entities from Syntage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entities?${params}`, {
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
      "@id": "string",
      "@type": "string",
      "createdAt": "string",
      "credential": {},
      "id": "string",
      "tags": [
        {}
      ],
      "taxpayer": {},
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Entities action reference](actions/list-entities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/syntage/latest/actions/list-entities).
