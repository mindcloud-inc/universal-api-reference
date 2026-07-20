# respond.io Universal API Examples

These examples use the MindCloud API key and respond.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact

Retrieves a contact from respond.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-contact?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-contact?${params}`, {
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
      "assignee": {},
      "countryCode": "string",
      "createdAt": 1,
      "customFields": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isBlocked": true,
      "language": "string",
      "lastName": "Chen",
      "lifecycle": "string",
      "locale": "string",
      "phone": "string",
      "profilePic": "string",
      "status": "string",
      "tags": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/respondio/latest/actions/get-contact).

## Add Tags

Adds tags to a contact in respond.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/add-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "tags": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/add-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "tags": "string"
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
      "contactId": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Tags action reference](actions/add-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/respondio/latest/actions/add-tags).
