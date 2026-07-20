# OTO Universal API Examples

These examples use the MindCloud API key and OTO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account information from the OTO API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-account-info?${params}`, {
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
      "accountType": "string",
      "CRDocStatus": "string",
      "email": "ava@example.com",
      "freelanceDocStatus": "string",
      "mobileNumber": "string",
      "name": "Ava Chen",
      "packageName": "Ava Chen",
      "remainingCredit": 1,
      "remainingFreeShipments": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oTO/latest/actions/get-account-info).

## Add Box

Creates a new box in OTO.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/add-box" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "length": 1,
  "width": 1,
  "height": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oTO/latest/actions/add-box', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "length": 1,
    "width": 1,
    "height": 1
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Box action reference](actions/add-box.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oTO/latest/actions/add-box).
