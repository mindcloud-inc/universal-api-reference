# Zoho Invoice Universal API Examples

These examples use the MindCloud API key and Zoho Invoice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Zoho Invoice.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-organizations?${params}`, {
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
      "contactName": "Ava Chen",
      "country": "string",
      "countryCode": "string",
      "currencyCode": "string",
      "currencySymbol": "string",
      "email": "ava@example.com",
      "isOrgActive": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "orgType": "string",
      "timeZone": "string",
      "timeZoneFormatted": "string",
      "version": "string",
      "versionFormatted": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoInvoice/latest/actions/list-organizations).

## Create Contact

Creates a contact in Zoho Invoice.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactName": "Acme Corp"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactName": "Acme Corp"
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
      "companyName": "Ava Chen",
      "contactId": "string",
      "contactName": "Ava Chen",
      "contactType": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerName": "Ava Chen",
      "customerSubType": "string",
      "email": "ava@example.com",
      "hasAttachment": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "mobile": "string",
      "phone": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoInvoice/latest/actions/create-contact).
