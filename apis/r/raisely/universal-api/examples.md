# Raisely Universal API Examples

These examples use the MindCloud API key and Raisely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Campaigns

Retrieves campaigns from Raisely.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaigns?${params}`, {
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
      "allowExperiments": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "feeTotal": 1,
      "goal": 1,
      "grandTotal": 1,
      "mode": "string",
      "name": "Ava Chen",
      "nonSelfDonationTotal": 1,
      "organisationUuid": "string",
      "path": "string",
      "primaryDomain": "string",
      "profile": {
        "currency": "string",
        "goal": 1,
        "name": "Ava Chen",
        "path": "string",
        "status": "string",
        "total": 1,
        "totalPercent": 1,
        "type": "string",
        "uuid": "string"
      },
      "publicKey": "string",
      "status": "string",
      "theme": "string",
      "total": 1,
      "totalPercent": 1,
      "url": "https://example.com",
      "uuid": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Campaigns action reference](actions/list-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/raisely/latest/actions/list-campaigns).

## Create Donation

Creates a new donation in Raisely.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/create-donation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.currency": "string",
  "data.email": "ava@example.com",
  "data.method": "string",
  "data.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/create-donation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.currency": "string",
    "data.email": "ava@example.com",
    "data.method": "string",
    "data.type": "string"
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
      "amount": 1,
      "anonymous": true,
      "campaignUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "fee": 1,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "lastName": "Chen",
      "message": "string",
      "method": "string",
      "mode": "string",
      "preferredName": "Ava Chen",
      "profileUuid": "string",
      "publicAmount": 1,
      "publicFee": 1,
      "status": "string",
      "subscriptionUuid": "string",
      "total": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Donation action reference](actions/create-donation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/raisely/latest/actions/create-donation).
