# Universe: List Event Discount Codes

Retrieves discount codes for a specific Universe event.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-discount-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-discount-codes?connectionId=$CONNECTION_ID&query=query%20ListEventDiscountCodes(%24eventId%3A%20ID!%2C%20%24searchQuery%3A%20String)%20%7B%0A%20%20eventDiscountCodes(listingId%3A%20%24eventId%2C%20searchQuery%3A%20%24searchQuery)%20%7B%0A%20%20%20%20nodes%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20code%0A%20%20%20%20%20%20state%0A%20%20%20%20%20%20quantity%0A%20%20%20%20%20%20remaining%0A%20%20%20%20%20%20used%0A%20%20%20%20%20%20percent%0A%20%20%20%20%20%20fixed%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListEventDiscountCodes($eventId: ID!, $searchQuery: String) {\n  eventDiscountCodes(listingId: $eventId, searchQuery: $searchQuery) {\n    nodes {\n      id\n      code\n      state\n      quantity\n      remaining\n      used\n      percent\n      fixed\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-discount-codes?${params}`, {
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
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an event discount-code example for this action. Default: `query ListEventDiscountCodes($eventId: ID!, $searchQuery: String) {\n  eventDiscountCodes(listingId: $eventId, searchQuery: $searchQuery) {\n    nodes {\n      id\n      code\n      state\n      quantity\n      remaining\n      used\n      percent\n      fixed\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default discount-code query. Default: `{"eventId":"EVENT_ID","searchQuery":""}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-discount-codes.md) for the provider-specific parameters and requirements.

