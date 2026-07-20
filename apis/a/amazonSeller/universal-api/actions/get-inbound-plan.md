# Amazon Seller: Get Inbound Plan

Retrieves an inbound plan from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-inbound-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-inbound-plan?connectionId=$CONNECTION_ID&inboundPlanId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboundPlanId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-inbound-plan?${params}`, {
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
| `inboundPlanId` | string | yes | Identifier for an inbound plan. |

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
        "addressLine2": "string",
        "city": "string",
        "companyName": "Ava Chen",
        "countryCode": "string",
        "email": "ava@example.com",
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
| `sourceAddress.addressLine2` | string |  |
| `sourceAddress.city` | string |  |
| `sourceAddress.companyName` | string |  |
| `sourceAddress.countryCode` | string |  |
| `sourceAddress.email` | string |  |
| `sourceAddress.name` | string |  |
| `sourceAddress.phoneNumber` | string |  |
| `sourceAddress.postalCode` | string |  |
| `sourceAddress.stateOrProvinceCode` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET inbound/fba/2024-03-20/inboundPlans/:inboundPlanId` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbound-plan.md) for the provider-specific parameters and requirements.

