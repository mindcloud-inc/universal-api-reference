# Qualiobee Universal API Examples

These examples use the MindCloud API key and Qualiobee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Qualiobee.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-customers?${params}`, {
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
      "conventions": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "isIndividual": true,
      "lastName": "Chen",
      "learners": [
        {}
      ],
      "location": {
        "addressLine1": "string",
        "addressLine2": "string",
        "archiveDate": "2026-05-07T12:00:00.000Z",
        "city": "string",
        "country": "string",
        "creationDate": "2026-05-07T12:00:00.000Z",
        "postCode": "string",
        "updateDate": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "naf": "string",
      "name": "Ava Chen",
      "note": "string",
      "phoneNumber": "string",
      "qualiobee": {
        "businessTitle": "string",
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "organization": {
          "deleteDate": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        },
        "uuid": "string"
      },
      "siret": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qualiobee/latest/actions/list-customers).

## Create Customer

Creates a new customer in Qualiobee.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationUuid": "string",
  "name": "Ava Chen",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationUuid": "string",
    "name": "Ava Chen",
    "firstName": "Ava",
    "lastName": "Chen",
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
      "conventions": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "isIndividual": true,
      "lastName": "Chen",
      "learners": {
        "creationDate": "2026-05-07T12:00:00.000Z",
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "externalId": "string",
        "firstName": "Ava",
        "jobStatus": "string",
        "lastName": "Chen",
        "needsAdaptation": true,
        "note": "string",
        "phoneNumber": "string",
        "type": "string",
        "updateDate": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "location": {
        "addressLine1": "string",
        "addressLine2": "string",
        "archiveDate": "2026-05-07T12:00:00.000Z",
        "city": "string",
        "country": "string",
        "creationDate": "2026-05-07T12:00:00.000Z",
        "postCode": "string",
        "updateDate": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "naf": "string",
      "name": "Ava Chen",
      "note": "string",
      "phoneNumber": "string",
      "siret": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qualiobee/latest/actions/create-customer).
