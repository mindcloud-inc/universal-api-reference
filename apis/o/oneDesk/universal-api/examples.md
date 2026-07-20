# OneDesk Universal API Examples

These examples use the MindCloud API key and OneDesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization Profile And Policy

Retrieves organization profile and policy from OneDesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-organization-profile-and-policy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-organization-profile-and-policy?${params}`, {
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
      "dateFormat": "string",
      "defaultThreadVisibilityType": "string",
      "organizationName": "Ava Chen",
      "organizationUri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Organization Profile And Policy action reference](actions/get-organization-profile-and-policy.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneDesk/latest/actions/get-organization-profile-and-policy).

## Create Customer

Creates a customer in OneDesk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneDesk/latest/actions/create-customer).
