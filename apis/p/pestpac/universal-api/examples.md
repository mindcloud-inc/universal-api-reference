# PestPac Universal API Examples

These examples use the MindCloud API key and PestPac connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## CompanySetup



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/company-setup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/company-setup?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [CompanySetup action reference](actions/company-setup.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pestpac/latest/actions/company-setup).

## Create Contact



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lastName": "Chen",
  "firstName": "Ava",
  "locationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lastName": "Chen",
    "firstName": "Ava",
    "locationId": 1
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
      "Address": "string",
      "Address2": "string",
      "AlternatePhone": "string",
      "AlternatePhoneExtension": "string",
      "AnniversaryDate": "string",
      "BirthDate": "string",
      "City": "string",
      "Comment": "string",
      "Company": "string",
      "ContactID": 1,
      "ContactType": "string",
      "EMail": "ava@example.com",
      "Fax": "string",
      "FaxExtension": "string",
      "FirstName": "Ava",
      "HomeAddress": "string",
      "HomeAddress2": "string",
      "HomeCity": "string",
      "HomePhone": "string",
      "HomePhoneExtension": "string",
      "HomeState": "string",
      "HomeZip": "string",
      "JobTitle": "string",
      "LastName": "Chen",
      "MobilePhone": "string",
      "MobilePhoneExtension": "string",
      "NameofAssistant": "Ava Chen",
      "NameofSpouse": "Ava Chen",
      "Nickname": "Ava Chen",
      "Phone": "string",
      "PhoneExtension": "string",
      "PronunciationOfName": "Ava Chen",
      "State": "string",
      "Title": "string",
      "UserDefinedFields": [
        "string"
      ],
      "Zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pestpac/latest/actions/create-contact).
