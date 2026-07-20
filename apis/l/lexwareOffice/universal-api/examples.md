# Lexware Office Universal API Examples

These examples use the MindCloud API key and Lexware Office connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Profile Information

Retrieves profile information from Lexware Office.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-profile-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-profile-information?${params}`, {
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
      "businessFeatures": [
        "string"
      ],
      "connectionId": "string",
      "created": {
        "date": "2026-05-07T12:00:00.000Z",
        "userEmail": "ava@example.com",
        "userId": "string",
        "userName": "Ava Chen"
      },
      "organizationId": "string",
      "smallBusiness": true,
      "taxType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Profile Information action reference](actions/retrieve-profile-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lexwareOffice/latest/actions/retrieve-profile-information).

## Create Article

Creates a new article in Lexware Office.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "type": "string",
  "unitName": "Ava Chen",
  "price.leadingPrice": "NET",
  "price.taxRate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "type": "string",
    "unitName": "Ava Chen",
    "price.leadingPrice": "NET",
    "price.taxRate": 1
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
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resourceUri": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Article action reference](actions/create-article.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lexwareOffice/latest/actions/create-article).
