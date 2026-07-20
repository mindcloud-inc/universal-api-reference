# Streamtime Universal API Examples

These examples use the MindCloud API key and Streamtime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organisation



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-organisation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-organisation?${params}`, {
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
      "address": {},
      "country": {},
      "currency": {},
      "domain": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Organisation action reference](actions/get-organisation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/streamtime/latest/actions/get-organisation).

## Create Company



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taxNumber": "NZ123-456-789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taxNumber": "NZ123-456-789"
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
      "branchId": 1,
      "branchName": "Ava Chen",
      "companyLeadUserId": 1,
      "companyStatus": {},
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone1": "string",
      "phone2": "string",
      "rateCardId": 1,
      "taxNumber": "string",
      "websiteAddress": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/streamtime/latest/actions/create-company).
