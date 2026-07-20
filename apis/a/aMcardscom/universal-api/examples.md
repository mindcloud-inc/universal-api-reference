# AMcards.com Universal API Examples

These examples use the MindCloud API key and AMcards.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves authorized user records from AMcards.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-users?${params}`, {
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
      "addressLine1": "string",
      "addressLine2": "string",
      "city": "string",
      "country": "string",
      "credits": 1,
      "dateJoined": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "lastTemplateUpdated": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "postage": {
        "bigcardCost": 1,
        "domesticCost": 1,
        "domesticCountries": [
          "string"
        ],
        "internationalCost": 1,
        "postcardCost": 1
      },
      "postal": "string",
      "resourceUri": "string",
      "showUpgradeMessage": true,
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aMcardscom/latest/actions/list-users).

## Create Contact

Creates a new contact in AMcards.com.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groups[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groups[]": ["string"]
  })
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

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aMcardscom/latest/actions/create-contact).
