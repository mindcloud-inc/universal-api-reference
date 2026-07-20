# Salespanel Universal API Examples

These examples use the MindCloud API key and Salespanel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from your Salespanel account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-contacts?${params}`, {
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
      "acquisitionDetails": {
        "landingIpAddress": "string",
        "landingLocation": {
          "country": "string",
          "countryCode": "string"
        },
        "landingUserAgent": {
          "browser": "string",
          "device": "string",
          "deviceOs": "string"
        },
        "source": "string"
      },
      "companyDetails": {
        "category": "string",
        "domain": "string",
        "industry": "string",
        "location": "string",
        "name": "Ava Chen",
        "website": "string"
      },
      "contactId": "string",
      "personDetails": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "gender": "string",
        "lastName": "Chen",
        "location": "string",
        "name": "Ava Chen",
        "organization": "string",
        "title": "string"
      },
      "webActivitySummary": {
        "firstSeen": "2026-05-07T12:00:00.000Z",
        "lastSeen": "2026-05-07T12:00:00.000Z",
        "totalPageVisits": 1,
        "totalWebsiteSessions": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salespanel/latest/actions/list-contacts).

## Identify Contact

Identifies a contact in Salespanel by associating an email.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/identify-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/identify-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Identify Contact action reference](actions/identify-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salespanel/latest/actions/identify-contact).
