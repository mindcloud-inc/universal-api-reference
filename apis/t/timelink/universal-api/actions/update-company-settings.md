# Timelink: Update Company Settings

Updates company settings in the Timelink workspace.

```
PUT https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-company-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-company-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-company-settings', {
  method: 'PUT',
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
| `vatid` | object |  |
| `zip` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `PATCH /company/settings` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company-settings.md) for the provider-specific parameters and requirements.

