# retailCRM: Get Customer

Retrieves a customer from retailCRM by external ID.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-customer?connectionId=$CONNECTION_ID&externalId=string&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-customer?${params}`, {
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
| `externalId` | string | yes |  |
| `by` | list | no | One of: `externalId`, `id`. Default: `externalId`. |
| `site` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averageSumm": 1,
      "bad": true,
      "contragent": {
        "contragentType": "string"
      },
      "createdAt": "string",
      "customerSubscriptions": [
        {
          "subscribed": true,
          "subscription": {
            "active": true,
            "autoSubscribe": true,
            "channel": "string",
            "code": "string",
            "id": 1,
            "name": "Ava Chen",
            "ordering": 1
          }
        }
      ],
      "customFields": [
        "string"
      ],
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "id": 1,
      "isContact": true,
      "lastName": "Chen",
      "managerId": 1,
      "marginSumm": 1,
      "mgCustomers": [
        "string"
      ],
      "ordersCount": 1,
      "personalDiscount": 1,
      "phones": [
        {
          "number": "string"
        }
      ],
      "segments": [
        "string"
      ],
      "site": "string",
      "tags": [
        "string"
      ],
      "totalSumm": 1,
      "type": "string",
      "vip": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageSumm` | number |  |
| `bad` | boolean |  |
| `contragent.contragentType` | string |  |
| `createdAt` | string |  |
| `customerSubscriptions[].subscribed` | boolean |  |
| `customerSubscriptions[].subscription.active` | boolean |  |
| `customerSubscriptions[].subscription.autoSubscribe` | boolean |  |
| `customerSubscriptions[].subscription.channel` | string |  |
| `customerSubscriptions[].subscription.code` | string |  |
| `customerSubscriptions[].subscription.id` | number |  |
| `customerSubscriptions[].subscription.name` | string |  |
| `customerSubscriptions[].subscription.ordering` | number |  |
| `customFields` | array |  |
| `email` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isContact` | boolean |  |
| `lastName` | string |  |
| `managerId` | number |  |
| `marginSumm` | number |  |
| `mgCustomers` | array |  |
| `ordersCount` | number |  |
| `personalDiscount` | number |  |
| `phones[].number` | string |  |
| `segments` | array |  |
| `site` | string |  |
| `tags` | array |  |
| `totalSumm` | number |  |
| `type` | string |  |
| `vip` | boolean |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /customers/:externalId` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

