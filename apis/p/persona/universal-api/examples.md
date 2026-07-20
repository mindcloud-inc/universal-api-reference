# Persona Universal API Examples

These examples use the MindCloud API key and Persona connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inquiries



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-inquiries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-inquiries?${params}`, {
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

See the full [List Inquiries action reference](actions/list-inquiries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/persona/latest/actions/list-inquiries).

## Add Account Tag



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/persona/latest/actions/add-account-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "act_123",
  "tagName": "mindcloud-tag-a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/persona/latest/actions/add-account-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "act_123",
    "tagName": "mindcloud-tag-a"
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
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Account Tag action reference](actions/add-account-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/persona/latest/actions/add-account-tag).
