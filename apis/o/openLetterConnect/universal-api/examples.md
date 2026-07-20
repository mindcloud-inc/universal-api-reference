# Open Letter Connect Universal API Examples

These examples use the MindCloud API key and Open Letter Connect connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Product Types

Retrieves product types from Open Letter Connect.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-types?${params}`, {
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
      "id": "string",
      "productType": "string",
      "size": [
        {
          "id": "string",
          "size": "string"
        }
      ],
      "windowed": true
    }
  ],
  "meta": {}
}
```

See the full [Get Product Types action reference](actions/get-product-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openLetterConnect/latest/actions/get-product-types).

## Create Contact

Creates a contact in Open Letter Connect.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-contact', {
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
      "address1": "string",
      "address2": "string",
      "addressStatus": "string",
      "city": "string",
      "companyName": "Ava Chen",
      "ContactLabels": [
        {
          "id": "string",
          "title": "string"
        }
      ],
      "createdAt": "string",
      "email": "ava@example.com",
      "extension": "string",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "isLiveMode": true,
      "isVerified": true,
      "lastMailedDate": "string",
      "lastMailedStatus": "string",
      "lastName": "Chen",
      "orgId": "string",
      "phoneNo": "string",
      "state": "string",
      "websiteUrl": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openLetterConnect/latest/actions/create-contact).
