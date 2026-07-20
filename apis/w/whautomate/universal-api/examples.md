# Whautomate Universal API Examples

These examples use the MindCloud API key and Whautomate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Locations

Retrieves locations from Whautomate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/list-locations?${params}`, {
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
      "district": "string",
      "id": "string",
      "phone": "string",
      "postalCode": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Locations action reference](actions/list-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whautomate/latest/actions/list-locations).

## Add Client

Creates a new client in Whautomate.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/add-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fullName": "Ava Chen",
  "primaryLocation": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/add-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fullName": "Ava Chen",
    "primaryLocation": {}
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
      "address": "string",
      "addressType": "string",
      "clientId": "string",
      "company": {},
      "contactType": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emergencyName": "Ava Chen",
      "emergencyPhone": "string",
      "emergencyRelationType": "string",
      "fullName": "Ava Chen",
      "gender": "string",
      "id": "string",
      "identificationNumber": "string",
      "maritalStatus": "string",
      "notes": "string",
      "phone": "string",
      "preferredLanguage": "string",
      "preferredName": "Ava Chen",
      "primaryLocation": {},
      "referralSource": "string",
      "registrationDate": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "taxIdNumber": "string",
      "taxIdType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Client action reference](actions/add-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whautomate/latest/actions/add-client).
