# Timelink: Create Client

Creates a client in the Timelink workspace.

```
POST https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-client', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `ext_tool_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "company": {
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
      },
      "companyId": "string",
      "createdAt": "string",
      "extToolId": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `company.address` | string |  |
| `company.autoupdateQuantity` | boolean |  |
| `company.city` | string |  |
| `company.color` | object |  |
| `company.country` | object |  |
| `company.createdAt` | string |  |
| `company.deletedAt` | object |  |
| `company.email` | string |  |
| `company.forceOauth` | boolean |  |
| `company.hasDemoData` | boolean |  |
| `company.id` | string |  |
| `company.industry` | string |  |
| `company.invoiceEmail` | string |  |
| `company.language` | object |  |
| `company.licenses` | number |  |
| `company.logo` | object |  |
| `company.name` | string |  |
| `company.oauth` | object |  |
| `company.oauthProvider` | object |  |
| `company.phone` | string |  |
| `company.pullProvider` | object |  |
| `company.pushIntegration` | object |  |
| `company.pushProvider` | object |  |
| `company.requiredFields[]` | string |  |
| `company.settings` | object |  |
| `company.sizeOfCompany` | string |  |
| `company.stripeExists` | boolean |  |
| `company.subscription.endsAt` | object |  |
| `company.subscription.pastDue` | object |  |
| `company.subscription.product` | string |  |
| `company.subscription.quantity` | object |  |
| `company.subscription.status` | string |  |
| `company.subscription.trial` | boolean |  |
| `company.subscription.trialEndsAt` | string |  |
| `company.trialEndsAt` | string |  |
| `company.updatedAt` | string |  |
| `company.vatid` | object |  |
| `company.zip` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `extToolId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `POST /clients` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

