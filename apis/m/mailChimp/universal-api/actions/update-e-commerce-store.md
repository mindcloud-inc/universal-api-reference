# Mailchimp: Update E-commerce Store

Updates an existing e-commerce store in Mailchimp.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-e-commerce-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-e-commerce-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "store_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-e-commerce-store', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "store_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `store_id` | string | yes |  |
| `name` | string | no |  |
| `platform` | string | no |  |
| `domain` | string | no |  |
| `is_syncing` | boolean | no |  |
| `email_address` | string | no |  |
| `currency_code` | string | no |  |
| `money_format` | string | no |  |
| `primary_locale` | string | no |  |
| `timezone` | string | no |  |
| `phone` | string | no |  |
| `address` | object | no |  |
| `address.address1` | string | no |  |
| `address.address2` | string | no |  |
| `address.city` | string | no |  |
| `address.province` | string | no |  |
| `address.province_code` | string | no |  |
| `address.postal_code` | string | no |  |
| `address.country` | string | no |  |
| `address.country_code` | string | no |  |
| `address.longitude` | number | no |  |
| `address.latitude` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "countryCode": "string",
        "latitude": 1,
        "longitude": 1,
        "postalCode": "string",
        "province": "string",
        "provinceCode": "string"
      },
      "automations": {
        "abandonedBrowse": {
          "isSupported": true
        },
        "abandonedCart": {
          "isSupported": true
        }
      },
      "createdAt": "string",
      "currencyCode": "string",
      "domain": "string",
      "emailAddress": "ava@example.com",
      "id": "string",
      "isSyncing": true,
      "links": [
        [
          {}
        ]
      ],
      "listId": "string",
      "listIsActive": true,
      "moneyFormat": "string",
      "name": "Ava Chen",
      "phone": "string",
      "platform": "string",
      "primaryLocale": "string",
      "timezone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address.address1` | string |  |
| `address.address2` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.countryCode` | string |  |
| `address.latitude` | number |  |
| `address.longitude` | number |  |
| `address.postalCode` | string |  |
| `address.province` | string |  |
| `address.provinceCode` | string |  |
| `automations` | object |  |
| `automations.abandonedBrowse` | object |  |
| `automations.abandonedBrowse.isSupported` | boolean |  |
| `automations.abandonedCart` | object |  |
| `automations.abandonedCart.isSupported` | boolean |  |
| `createdAt` | string |  |
| `currencyCode` | string |  |
| `domain` | string |  |
| `emailAddress` | string |  |
| `id` | string |  |
| `isSyncing` | boolean |  |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].targetSchema` | string |  |
| `listId` | string |  |
| `listIsActive` | boolean |  |
| `moneyFormat` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `platform` | string |  |
| `primaryLocale` | string |  |
| `timezone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Mailchimp API, this operation is `PATCH ecommerce/stores/:store_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-e-commerce-store.md) for the provider-specific parameters and requirements.

