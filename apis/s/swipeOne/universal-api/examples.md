# Swipe One Universal API Examples

These examples use the MindCloud API key and Swipe One connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact Fields



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact-fields?${params}`, {
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
      "key": "string",
      "label": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Contact Fields action reference](actions/get-contact-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swipeOne/latest/actions/get-contact-fields).

## Create Contact



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
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
      "data": {
        "contact": {
          "_id": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": {
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          },
          "email": "ava@example.com",
          "firstName": "Ava",
          "fullName": "Ava Chen",
          "lastName": "Chen",
          "tags": [
            "string"
          ],
          "workspaceId": "string"
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swipeOne/latest/actions/create-contact).
