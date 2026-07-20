# Socie Universal API Examples

These examples use the MindCloud API key and Socie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Members



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socie/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socie/latest/actions/list-members?${params}`, {
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
      "emailAddress": "ava@example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Members action reference](actions/list-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/socie/latest/actions/list-members).

## Add Additional Field



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-additional-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-additional-field', {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isEditableByMember": true,
      "isMandatoryForMember": true,
      "isVisibleInApp": true,
      "name": "Ava Chen",
      "orderNumber": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Additional Field action reference](actions/add-additional-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/socie/latest/actions/add-additional-field).
