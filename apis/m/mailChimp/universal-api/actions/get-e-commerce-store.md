# Mailchimp: Get E-commerce Store

Retrieves an e-commerce store from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-e-commerce-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-e-commerce-store?connectionId=$CONNECTION_ID&store_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "store_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-e-commerce-store?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `store_id` | string | yes |  |
| `fields` | string | no |  |
| `exclude_fields` | string | no |  |

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

Through the native Mailchimp API, this operation is `GET ecommerce/stores/:store_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-e-commerce-store.md) for the provider-specific parameters and requirements.

