# Universe: Upsert Event Discounts

Creates or updates discounts for a Universe event.

```
PUT https://connect.mindcloud.co/v1/universal/universe/latest/actions/upsert-event-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/universe/latest/actions/upsert-event-discounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation UpsertEventDiscounts($input: EventDiscountsUpsertInput!) {\n  eventDiscountsUpsert(input: $input) {\n    errors\n    discounts {\n      id\n      code\n      state\n      quantity\n      remaining\n      used\n      percent\n      fixed\n      redemptionType\n      rates {\n        id\n        name\n      }\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/universe/latest/actions/upsert-event-discounts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation UpsertEventDiscounts($input: EventDiscountsUpsertInput!) {\n  eventDiscountsUpsert(input: $input) {\n    errors\n    discounts {\n      id\n      code\n      state\n      quantity\n      remaining\n      used\n      percent\n      fixed\n      redemptionType\n      rates {\n        id\n        name\n      }\n    }\n  }\n}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an event discounts upsert mutation for this action. Default: `mutation UpsertEventDiscounts($input: EventDiscountsUpsertInput!) {\n  eventDiscountsUpsert(input: $input) {\n    errors\n    discounts {\n      id\n      code\n      state\n      quantity\n      remaining\n      used\n      percent\n      fixed\n      redemptionType\n      rates {\n        id\n        name\n      }\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default discount upsert mutation. Default: `{"input":{"discounts":[{"attributes":{"code":"DISCOUNT_CODE","state":"ACTIVE","percent":10,"rateIds":["RATE_ID"],"quantity":5,"redemptionType":"PERCENT"}}],"listingId":"EVENT_ID"}}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-event-discounts.md) for the provider-specific parameters and requirements.

