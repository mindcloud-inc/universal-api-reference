# Amazon Seller: List Inbound Plans

Retrieves inbound plans from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-inbound-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-inbound-plans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-inbound-plans?${params}`, {
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
| `status` | list<string> | no | The status of an inbound plan. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "inboundPlanId": "string",
      "lastUpdatedAt": "string",
      "marketplaceIds": [
        "string"
      ],
      "name": "Ava Chen",
      "sourceAddress": {
        "addressLine1": "string",
        "city": "string",
        "countryCode": "string",
        "name": "Ava Chen",
        "phoneNumber": "string",
        "postalCode": "string",
        "stateOrProvinceCode": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `inboundPlanId` | string |  |
| `lastUpdatedAt` | string |  |
| `marketplaceIds[]` | string |  |
| `name` | string |  |
| `sourceAddress.addressLine1` | string |  |
| `sourceAddress.city` | string |  |
| `sourceAddress.countryCode` | string |  |
| `sourceAddress.name` | string |  |
| `sourceAddress.phoneNumber` | string |  |
| `sourceAddress.postalCode` | string |  |
| `sourceAddress.stateOrProvinceCode` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET inbound/fba/2024-03-20/inboundPlans` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inbound-plans.md) for the provider-specific parameters and requirements.

