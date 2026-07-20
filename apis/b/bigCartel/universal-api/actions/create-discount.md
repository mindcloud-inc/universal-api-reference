# Big Cartel: Create Discount

Creates a discount in Big Cartel.

```
POST https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-discount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "name": "Ava Chen",
  "code": "string",
  "requirementType": "string",
  "expirationType": "string",
  "rewardType": "string",
  "applicationType": "string",
  "percentDiscount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-discount', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "name": "Ava Chen",
    "code": "string",
    "requirementType": "string",
    "expirationType": "string",
    "rewardType": "string",
    "applicationType": "string",
    "percentDiscount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Big Cartel account ID. |
| `name` | string | yes |  |
| `code` | string | yes |  |
| `requirementType` | string | yes |  |
| `expirationType` | string | yes |  |
| `rewardType` | string | yes |  |
| `applicationType` | string | yes |  |
| `percentDiscount` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "activeAt": "string",
        "applicationType": "string",
        "code": "string",
        "expirationType": "string",
        "expiresAt": "string",
        "includesFreeShipping": true,
        "name": "Ava Chen",
        "percentDiscount": 1,
        "requirementType": "string",
        "rewardType": "string",
        "useCount": 1
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "relationships": {
        "categories": {
          "data": [
            {}
          ]
        },
        "products": {
          "data": [
            {}
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.activeAt` | string |  |
| `attributes.applicationType` | string |  |
| `attributes.code` | string |  |
| `attributes.expirationType` | string |  |
| `attributes.expiresAt` | string |  |
| `attributes.includesFreeShipping` | boolean |  |
| `attributes.name` | string |  |
| `attributes.percentDiscount` | number |  |
| `attributes.requirementType` | string |  |
| `attributes.rewardType` | string |  |
| `attributes.useCount` | number |  |
| `id` | string |  |
| `links.self` | string |  |
| `relationships.categories.data` | array<object> |  |
| `relationships.products.data` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `POST /v1/accounts/[:account-id]/discounts` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-discount.md) for the provider-specific parameters and requirements.

