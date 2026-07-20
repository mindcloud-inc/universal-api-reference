# Sendblue Universal API Examples

These examples use the MindCloud API key and Sendblue connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact

Retrieves a contact from Sendblue by phone number.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-contact?connectionId=$CONNECTION_ID&phoneNumber=%2B14155550123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "+14155550123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-contact?${params}`, {
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
      "contact": {
        "companyName": "Ava Chen",
        "createdAt": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "phone": "string",
        "sendblueNumber": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendblue/latest/actions/get-contact).

## Add Webhooks

Adds webhooks to Sendblue.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/add-webhooks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhooks[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/add-webhooks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhooks[]": ["string"]
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
      "message": "string",
      "status": "string",
      "webhooks": {
        "receive": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Webhooks action reference](actions/add-webhooks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendblue/latest/actions/add-webhooks).
