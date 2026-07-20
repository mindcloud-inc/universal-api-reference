# Attio Universal API Examples

These examples use the MindCloud API key and Attio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Objects

Retrieves objects from Attio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-objects?${params}`, {
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
      "apiSlug": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "pluralNoun": "string",
      "singularNoun": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Objects action reference](actions/list-objects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/attio/latest/actions/list-objects).

## Assert List Entry by Parent

Creates or updates a list entry in Attio by parent record.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/attio/latest/actions/assert-list-entry-by-parent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list": "string",
  "parentObject": "string",
  "parentRecordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/assert-list-entry-by-parent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list": "string",
    "parentObject": "string",
    "parentRecordId": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "entryValues": {},
      "id": {},
      "parentObject": "string",
      "parentRecordId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assert List Entry by Parent action reference](actions/assert-list-entry-by-parent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/attio/latest/actions/assert-list-entry-by-parent).
