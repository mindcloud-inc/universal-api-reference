# Adalo Universal API Examples

These examples use the MindCloud API key and Adalo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Collection Records

Retrieves records from a specific Adalo collection.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adalo/latest/actions/list-collection-records?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=string&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "appId": "string",
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adalo/latest/actions/list-collection-records?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Collection Records action reference](actions/list-collection-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/adalo/latest/actions/list-collection-records).
