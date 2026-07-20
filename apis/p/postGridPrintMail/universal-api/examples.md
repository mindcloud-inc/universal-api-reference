# PostGrid Print & Mail Universal API Examples

These examples use the MindCloud API key and PostGrid Print & Mail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from PostGrid Print & Mail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-contacts?${params}`, {
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
      "addressStatus": "string",
      "city": "string",
      "country": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "live": true,
      "mailingLists": [
        {}
      ],
      "object": "string",
      "postalOrZip": "string",
      "provinceOrState": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postGridPrintMail/latest/actions/list-contacts).

## Create Bank Account

Creates a bank account in PostGrid Print & Mail.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-bank-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bankName": "Ava Chen",
  "bankCountryCode": "string",
  "accountNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-bank-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bankName": "Ava Chen",
    "bankCountryCode": "string",
    "accountNumber": "string"
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
      "accountNumberAndIDSHA256": "string",
      "accountNumberLast4": "string",
      "bankCountryCode": "string",
      "bankName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "live": true,
      "object": "string",
      "routingNumber": "string",
      "signatureText": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Bank Account action reference](actions/create-bank-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postGridPrintMail/latest/actions/create-bank-account).
