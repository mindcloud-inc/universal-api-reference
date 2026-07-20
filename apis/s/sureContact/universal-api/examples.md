# SureContact Universal API Examples

These examples use the MindCloud API key and SureContact connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves available contact lists from SureContact.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-lists?${params}`, {
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
      "contact_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "is_system": true,
      "name": "Ava Chen",
      "type": "string",
      "type_label": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sureContact/latest/actions/list-lists).

## Add Contacts to List

Adds contacts to an existing SureContact list.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/add-contacts-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactUuids[]": [
    "string"
  ],
  "listUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/add-contacts-to-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactUuids[]": ["string"],
    "listUuid": "string"
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
      "contact_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "is_system": true,
      "name": "Ava Chen",
      "type": "string",
      "type_label": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contacts to List action reference](actions/add-contacts-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sureContact/latest/actions/add-contacts-to-list).
