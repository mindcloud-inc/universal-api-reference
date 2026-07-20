# Pledge Universal API Examples

These examples use the MindCloud API key and Pledge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Pledge.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-organizations?${params}`, {
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
      "alias": "string",
      "city": "string",
      "country": "string",
      "disbursementType": "string",
      "id": "string",
      "lat": {},
      "logoUrl": "https://example.com",
      "lon": {},
      "mission": {},
      "name": "Ava Chen",
      "ngoId": "string",
      "postalCode": "string",
      "profileUrl": "https://example.com",
      "region": "string",
      "street1": "string",
      "street2": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pledge/latest/actions/list-organizations).

## Create Donation

Creates a donation in Pledge.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-donation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "amount": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-donation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "amount": "string",
    "organizationId": "string"
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
      "amount": "string",
      "beneficiaries": [
        {
          "alias": "string",
          "amount": "string",
          "cause": "string",
          "causes": [
            {
              "id": 1,
              "name": "Ava Chen",
              "parentId": {}
            }
          ],
          "city": "string",
          "country": "string",
          "disbursementType": "string",
          "id": "string",
          "lat": "string",
          "logoUrl": "https://example.com",
          "lon": "string",
          "mission": "string",
          "name": "Ava Chen",
          "ngoId": "string",
          "postalCode": "string",
          "profileUrl": "https://example.com",
          "region": "string",
          "street1": "string",
          "street2": "string",
          "sustainableDevelopmentGoals": [
            {
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "type": "string",
          "usdAmount": "string",
          "websiteUrl": "https://example.com"
        }
      ],
      "createdAt": "string",
      "currency": "string",
      "donationAmount": "string",
      "donationUsdAmount": "string",
      "email": "ava@example.com",
      "externalId": {},
      "feeUsdAmount": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "metadata": {},
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "phoneNumber": {},
      "status": "string",
      "tipAmount": "string",
      "tipUsdAmount": "string",
      "updatedAt": "string",
      "usdAmount": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Donation action reference](actions/create-donation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pledge/latest/actions/create-donation).
