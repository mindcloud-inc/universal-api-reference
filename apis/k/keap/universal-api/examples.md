# Keap Universal API Examples

These examples use the MindCloud API key and Keap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-company?connectionId=$CONNECTION_ID&company_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-company?${params}`, {
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
      "companyName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keap/latest/actions/get-company).

## Apply Tag To Contacts



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keap/latest/actions/apply-tag-to-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_ids": "string",
  "tag_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keap/latest/actions/apply-tag-to-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_ids": "string",
    "tag_id": "string"
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
      "results": {}
    }
  ],
  "meta": {}
}
```

See the full [Apply Tag To Contacts action reference](actions/apply-tag-to-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/keap/latest/actions/apply-tag-to-contacts).
