# Timelink: Get Company

Retrieves company details from the Timelink workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-company?${params}`, {
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
      "activeClientsCount": 1,
      "activeProjectsCount": 1,
      "activeServicesCount": 1,
      "activeUsersCount": 1,
      "address": "string",
      "autoupdateQuantity": true,
      "city": "string",
      "color": {},
      "country": {},
      "createdAt": "string",
      "deletedAt": {},
      "disabledClientsCount": 1,
      "disabledProjectsCount": 1,
      "disabledServicesCount": 1,
      "email": "ava@example.com",
      "forceOauth": true,
      "hasDemoData": true,
      "id": "string",
      "industry": "string",
      "invoiceEmail": "ava@example.com",
      "language": {},
      "licenses": 1,
      "logo": {},
      "name": "Ava Chen",
      "oauth": {},
      "oauthProvider": {},
      "phone": "string",
      "pullProvider": {},
      "pushIntegration": {},
      "pushProvider": {},
      "requiredFields": [
        "string"
      ],
      "settings": {},
      "sizeOfCompany": "string",
      "stripeExists": true,
      "subscription": {
        "endsAt": {},
        "pastDue": {},
        "product": "string",
        "quantity": {},
        "status": "string",
        "trial": true,
        "trialEndsAt": "string"
      },
      "trialEndsAt": "string",
      "updatedAt": "string",
      "usersCount": 1,
      "vatid": {},
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeClientsCount` | number |  |
| `activeProjectsCount` | number |  |
| `activeServicesCount` | number |  |
| `activeUsersCount` | number |  |
| `address` | string |  |
| `autoupdateQuantity` | boolean |  |
| `city` | string |  |
| `color` | object |  |
| `country` | object |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `disabledClientsCount` | number |  |
| `disabledProjectsCount` | number |  |
| `disabledServicesCount` | number |  |
| `email` | string |  |
| `forceOauth` | boolean |  |
| `hasDemoData` | boolean |  |
| `id` | string |  |
| `industry` | string |  |
| `invoiceEmail` | string |  |
| `language` | object |  |
| `licenses` | number |  |
| `logo` | object |  |
| `name` | string |  |
| `oauth` | object |  |
| `oauthProvider` | object |  |
| `phone` | string |  |
| `pullProvider` | object |  |
| `pushIntegration` | object |  |
| `pushProvider` | object |  |
| `requiredFields[]` | string |  |
| `settings` | object |  |
| `sizeOfCompany` | string |  |
| `stripeExists` | boolean |  |
| `subscription.endsAt` | object |  |
| `subscription.pastDue` | object |  |
| `subscription.product` | string |  |
| `subscription.quantity` | object |  |
| `subscription.status` | string |  |
| `subscription.trial` | boolean |  |
| `subscription.trialEndsAt` | string |  |
| `trialEndsAt` | string |  |
| `updatedAt` | string |  |
| `usersCount` | number |  |
| `vatid` | object |  |
| `zip` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `GET /company` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

