# Zoho Books Universal API Examples

These examples use the MindCloud API key and Zoho Books connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-organizations?${params}`, {
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
      "appList": [
        "string"
      ],
      "contactName": "Ava Chen",
      "country": "string",
      "countryCode": "string",
      "currencyCode": "string",
      "currencyId": "string",
      "currencySymbol": "string",
      "email": "ava@example.com",
      "isDefaultOrg": true,
      "isOrgActive": true,
      "languageCode": "string",
      "mode": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "orgType": "string",
      "planName": "Ava Chen",
      "pricePrecision": 1,
      "state": "string",
      "stateCode": "string",
      "timeZone": "string",
      "version": "string",
      "versionFormatted": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoBooks/latest/actions/list-organizations).

## Create Bill



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billNumber": "string",
  "organizationId": "string",
  "vendorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billNumber": "string",
    "organizationId": "string",
    "vendorId": "string"
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
      "bill": {
        "accountId": "string",
        "accountName": "Ava Chen",
        "attachmentName": "Ava Chen",
        "balance": 1,
        "billId": "string",
        "billingAddress": {},
        "billNumber": "string",
        "createdTime": "2026-05-07T12:00:00.000Z",
        "currencyCode": "string",
        "currencyId": "string",
        "currencySymbol": "string",
        "currentSubStatus": "string",
        "date": "2026-05-07T12:00:00.000Z",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "entityType": "string",
        "exchangeRate": 1,
        "lastModifiedTime": "2026-05-07T12:00:00.000Z",
        "lineItems": [
          {}
        ],
        "notes": "string",
        "paymentMade": 1,
        "pricePrecision": 1,
        "referenceNumber": "string",
        "status": "string",
        "subTotal": 1,
        "taxTotal": 1,
        "templateId": "string",
        "templateName": "Ava Chen",
        "total": 1,
        "vendorCreditsApplied": 1,
        "vendorId": "string",
        "vendorName": "Ava Chen"
      },
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bill action reference](actions/create-bill.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoBooks/latest/actions/create-bill).
