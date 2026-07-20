# Gumroad Universal API Examples

These examples use the MindCloud API key and Gumroad connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves the current user from Gumroad.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-user?${params}`, {
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
      "success": true,
      "user": {
        "bio": "string",
        "currencyType": "string",
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string",
        "links": [
          [
            "https://example.com"
          ]
        ],
        "name": "Ava Chen",
        "profileUrl": "https://example.com",
        "twitterHandle": "string",
        "url": "https://example.com",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gumroad/latest/actions/get-user).

## Create Custom Field

Creates a new custom field in Gumroad.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "name": "Ava Chen",
  "required": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "name": "Ava Chen",
    "required": true
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
      "customField": {
        "name": "Ava Chen",
        "required": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Custom Field action reference](actions/create-custom-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gumroad/latest/actions/create-custom-field).
