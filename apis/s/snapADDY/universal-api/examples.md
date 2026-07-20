# snapADDY Universal API Examples

These examples use the MindCloud API key and snapADDY connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-current-user?${params}`, {
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
      "isAdmin": true,
      "isTerminalUser": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "permissions": [
        "string"
      ],
      "profile": {},
      "userId": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snapADDY/latest/actions/get-current-user).

## Create Contact Item



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/create-contact-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attachments[]": [
    "string"
  ],
  "bcChecked": true,
  "bcImage": "string",
  "bcImageBackside": "string",
  "bcImageBacksideLocal": "string",
  "bcImageLocal": "string",
  "city": "string",
  "companySize": "string",
  "contactListId": "string",
  "country": "string",
  "customFields": {},
  "drawing": "string",
  "email": "ava@example.com",
  "facebook": "string",
  "fax": "string",
  "firstName": "Ava",
  "gender": 1,
  "image": "string",
  "industry": "string",
  "lastName": "Chen",
  "linkedin": "https://example.com",
  "mobile": "string",
  "note": "string",
  "organization": "string",
  "phone": "string",
  "poBox": "string",
  "position": "string",
  "revenue": "string",
  "state": "string",
  "street": "string",
  "title": "string",
  "twitter": "string",
  "vat": "string",
  "website": "string",
  "xing": "string",
  "zip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/create-contact-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attachments[]": ["string"],
    "bcChecked": true,
    "bcImage": "string",
    "bcImageBackside": "string",
    "bcImageBacksideLocal": "string",
    "bcImageLocal": "string",
    "city": "string",
    "companySize": "string",
    "contactListId": "string",
    "country": "string",
    "customFields": {},
    "drawing": "string",
    "email": "ava@example.com",
    "facebook": "string",
    "fax": "string",
    "firstName": "Ava",
    "gender": 1,
    "image": "string",
    "industry": "string",
    "lastName": "Chen",
    "linkedin": "https://example.com",
    "mobile": "string",
    "note": "string",
    "organization": "string",
    "phone": "string",
    "poBox": "string",
    "position": "string",
    "revenue": "string",
    "state": "string",
    "street": "string",
    "title": "string",
    "twitter": "string",
    "vat": "string",
    "website": "string",
    "xing": "string",
    "zip": "string"
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
      "attachments": [
        "string"
      ],
      "city": "string",
      "contactListId": "string",
      "country": "string",
      "created": "string",
      "customFields": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "organization": "string",
      "phone": "string",
      "position": "string",
      "updated": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact Item action reference](actions/create-contact-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snapADDY/latest/actions/create-contact-item).
