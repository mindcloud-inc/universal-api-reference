# Brevo Universal API Examples

These examples use the MindCloud API key and Brevo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-account?${params}`, {
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
      "address": {
        "city": "string",
        "country": "string",
        "street": "string",
        "zipCode": "string"
      },
      "companyName": "Ava Chen",
      "dateTimePreferences": {
        "dateFormat": "string",
        "timeFormat": "string",
        "timezone": "string"
      },
      "email": "ava@example.com",
      "enterprise": true,
      "firstName": "Ava",
      "language": "string",
      "lastName": "Chen",
      "organizationId": "string",
      "plan": [
        {
          "credits": 1,
          "creditsType": "string",
          "type": "string"
        }
      ],
      "planVerticals": [
        {
          "endDate": "string",
          "name": "Ava Chen",
          "planCategory": "string",
          "planType": "string",
          "startDate": "string",
          "status": "string",
          "users": {
            "purchasedSeats": "string",
            "usedSeats": "string"
          }
        }
      ],
      "relay": {
        "data": {
          "port": 1,
          "relay": "string",
          "userName": "Ava Chen"
        },
        "enabled": true
      },
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brevo/latest/actions/get-account).

## Activate Ecommerce



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/activate-ecommerce" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/activate-ecommerce', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Activate Ecommerce action reference](actions/activate-ecommerce.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brevo/latest/actions/activate-ecommerce).
