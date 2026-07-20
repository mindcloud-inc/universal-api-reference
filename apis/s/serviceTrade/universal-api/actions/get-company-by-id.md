# ServiceTrade: Get Company by ID

Retrieves a company from ServiceTrade by ID.

```
GET https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-company-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-company-by-id?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-company-by-id?${params}`, {
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
| `companyId` | number | yes | ID of the company to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "postalCode": "string",
        "state": "string",
        "street": "string"
      },
      "created": 1,
      "customer": true,
      "externalIds": {
        "quickbooks": "string"
      },
      "id": 1,
      "name": "Ava Chen",
      "partsVendor": true,
      "phoneNumber": "string",
      "primeContractor": true,
      "refNumber": "string",
      "serviceLinesProvided": [
        {
          "abbr": "string",
          "id": 1,
          "name": "Ava Chen",
          "trade": "string"
        }
      ],
      "status": "string",
      "updated": 1,
      "uri": "string",
      "vendor": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `address.street` | string |  |
| `created` | number |  |
| `customer` | boolean |  |
| `externalIds.quickbooks` | string |  |
| `id` | number |  |
| `name` | string |  |
| `partsVendor` | boolean |  |
| `phoneNumber` | string |  |
| `primeContractor` | boolean |  |
| `refNumber` | string |  |
| `serviceLinesProvided[].abbr` | string |  |
| `serviceLinesProvided[].id` | number |  |
| `serviceLinesProvided[].name` | string |  |
| `serviceLinesProvided[].trade` | string |  |
| `status` | string |  |
| `updated` | number |  |
| `uri` | string |  |
| `vendor` | boolean |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `GET company/:companyId` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-by-id.md) for the provider-specific parameters and requirements.

