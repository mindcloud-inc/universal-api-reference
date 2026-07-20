# Brevo: Get Account



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.street` | string |  |
| `address.zipCode` | string |  |
| `companyName` | string |  |
| `dateTimePreferences.dateFormat` | string |  |
| `dateTimePreferences.timeFormat` | string |  |
| `dateTimePreferences.timezone` | string |  |
| `email` | string |  |
| `enterprise` | boolean |  |
| `firstName` | string |  |
| `language` | string |  |
| `lastName` | string |  |
| `organizationId` | string |  |
| `plan[].credits` | number |  |
| `plan[].creditsType` | string |  |
| `plan[].type` | string |  |
| `planVerticals[].endDate` | string |  |
| `planVerticals[].name` | string |  |
| `planVerticals[].planCategory` | string |  |
| `planVerticals[].planType` | string |  |
| `planVerticals[].startDate` | string |  |
| `planVerticals[].status` | string |  |
| `planVerticals[].users.purchasedSeats` | string |  |
| `planVerticals[].users.usedSeats` | string |  |
| `relay.data.port` | number |  |
| `relay.data.relay` | string |  |
| `relay.data.userName` | string |  |
| `relay.enabled` | boolean |  |
| `userId` | number |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/account` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

