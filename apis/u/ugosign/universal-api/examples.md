# Ugosign Universal API Examples

These examples use the MindCloud API key and Ugosign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization

Retrieves an organization summary from Ugosign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-organization?${params}`, {
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
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "extraStorageGb": 1,
      "id": "string",
      "identityTokens": 1,
      "locale": "string",
      "overrunProtection": true,
      "slug": "string",
      "smsTokens": 1,
      "taxPercentage": "string",
      "title": "string",
      "trialEndsAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Organization action reference](actions/get-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ugosign/latest/actions/get-organization).

## Create Contact

Creates a new contact in Ugosign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "address": {
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "street": "string",
        "street2": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "gender": "string",
      "givenName": "Ava Chen",
      "id": "string",
      "phoneNumber": "string",
      "position": "string",
      "privateComment": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ugosign/latest/actions/create-contact).
