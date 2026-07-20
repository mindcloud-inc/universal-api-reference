# Routee: View all the available numbers

Retrieves all the available numbers from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-all-the-available-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-all-the-available-numbers?connectionId=$CONNECTION_ID&country=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-all-the-available-numbers?${params}`, {
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
| `country` | string | yes | The country of the recipient in ISO 3166-1 alpha 2 format. |
| `service` | string | no | The available services are "Sms" and "Voice" (case sensitive) |
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | number | no | The number of items to retrieve, default value is 20. |
| `sort` | string | no | The field name that will be used to sort the results. |
| `areaCode` | number | no | Area code is a 3-digit prefix applied only for US numbers(1-xxx-123456). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].activationCosts` | object |  |
| `content[].activationCosts.currency` | string |  |
| `content[].activationCosts.price` | number |  |
| `content[].chargeInterval` | number |  |
| `content[].country` | string |  |
| `content[].inboundCosts[]` | array<object> |  |
| `content[].inboundCosts[].currency` | string |  |
| `content[].inboundCosts[].price` | number |  |
| `content[].inboundCosts[].service` | string |  |
| `content[].monthlyCosts` | object |  |
| `content[].monthlyCosts.currency` | string |  |
| `content[].monthlyCosts.price` | number |  |
| `content[].msisdn` | string |  |
| `content[].services[]` | array<string> |  |
| `content[].tollFree` | boolean |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /numbers/available` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-all-the-available-numbers.md) for the provider-specific parameters and requirements.

