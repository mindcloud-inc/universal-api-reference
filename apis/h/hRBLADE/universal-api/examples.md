# HRBLADE Universal API Examples

These examples use the MindCloud API key and HRBLADE connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-user?${params}`, {
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
      "code": 1,
      "error": true,
      "response": {
        "data": {
          "agency": {
            "aiRequestsCount": 1,
            "aiRequestsLimit": 1,
            "clientType": "string",
            "companiesLimit": 1,
            "countryCode": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "id": 1,
            "interviewsLimit": 1,
            "planId": 1,
            "quantity": 1,
            "responsesLimit": 1,
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "usersLimit": 1,
            "videoDefinition": "string"
          },
          "country": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": 1,
          "lang": "string",
          "name": "Ava Chen",
          "recruitingOwner": 1,
          "role": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        },
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hRBLADE/latest/actions/get-user).

## Create Company



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "code": 1,
      "error": true,
      "response": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hRBLADE/latest/actions/create-company).
