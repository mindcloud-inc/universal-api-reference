# Bexio Universal API Examples

These examples use the MindCloud API key and Bexio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact

Retrieves a contact from Bexio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-contact?${params}`, {
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
      "address": "string",
      "addressAddition": {},
      "birthday": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "contactBranchIds": {},
      "contactGroupIds": "string",
      "contactTypeId": 1,
      "countryId": 1,
      "fax": "string",
      "houseNumber": "string",
      "id": 1,
      "isLead": true,
      "languageId": {},
      "mail": {},
      "mailSecond": {},
      "name1": "Ava Chen",
      "name2": "Ava Chen",
      "nr": "string",
      "ownerId": 1,
      "phoneFixed": {},
      "phoneFixedSecond": {},
      "phoneMobile": "string",
      "postcode": "string",
      "profileImage": "string",
      "remarks": "string",
      "salutationForm": {},
      "salutationId": 1,
      "skypeName": "Ava Chen",
      "streetName": "Ava Chen",
      "titleId": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bexio/latest/actions/get-contact).

## Create Contact

Creates a contact in Bexio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactTypeId": "1",
  "name1": "Example Company",
  "userId": "1",
  "ownerId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactTypeId": "1",
    "name1": "Example Company",
    "userId": "1",
    "ownerId": "1"
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
      "address": {},
      "addressAddition": {},
      "birthday": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "contactBranchIds": {},
      "contactGroupIds": {},
      "contactTypeId": 1,
      "countryId": {},
      "fax": "string",
      "houseNumber": {},
      "id": 1,
      "isLead": true,
      "languageId": {},
      "mail": "string",
      "mailSecond": "string",
      "name1": "Ava Chen",
      "name2": "Ava Chen",
      "nr": "string",
      "ownerId": 1,
      "phoneFixed": "string",
      "phoneFixedSecond": "string",
      "phoneMobile": "string",
      "postcode": "string",
      "profileImage": "string",
      "remarks": "string",
      "salutationForm": {},
      "salutationId": {},
      "skypeName": "Ava Chen",
      "streetName": {},
      "titleId": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bexio/latest/actions/create-contact).
