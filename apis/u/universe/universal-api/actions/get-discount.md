# Universe: Get Discount

Retrieves a specific discount from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-discount?connectionId=$CONNECTION_ID&query=query%20GetDiscount(%24discountId%3A%20ID!)%20%7B%0A%20%20discount(id%3A%20%24discountId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20code%0A%20%20%20%20state%0A%20%20%20%20quantity%0A%20%20%20%20remaining%0A%20%20%20%20used%0A%20%20%20%20percent%0A%20%20%20%20fixed%0A%20%20%20%20redemptionType%0A%20%20%20%20createdAt%0A%20%20%20%20updatedAt%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetDiscount($discountId: ID!) {\n  discount(id: $discountId) {\n    id\n    code\n    state\n    quantity\n    remaining\n    used\n    percent\n    fixed\n    redemptionType\n    createdAt\n    updatedAt\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-discount?${params}`, {
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
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is a discount detail example for this action. Default: `query GetDiscount($discountId: ID!) {\n  discount(id: $discountId) {\n    id\n    code\n    state\n    quantity\n    remaining\n    used\n    percent\n    fixed\n    redemptionType\n    createdAt\n    updatedAt\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default discount query. Default: `{"discountId":"DISCOUNT_ID"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-discount.md) for the provider-specific parameters and requirements.

