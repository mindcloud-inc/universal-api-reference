# Universe: Get Membership

Retrieves a specific membership from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-membership?connectionId=$CONNECTION_ID&query=query%20GetMembership(%24membershipId%3A%20ID!)%20%7B%0A%20%20membership(id%3A%20%24membershipId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20organizationName%0A%20%20%20%20state%0A%20%20%20%20allEvents%0A%20%20%20%20eventIds%0A%20%20%20%20listingIds%0A%20%20%20%20owner%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20name%0A%20%20%20%20%20%20slug%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetMembership($membershipId: ID!) {\n  membership(id: $membershipId) {\n    id\n    organizationName\n    state\n    allEvents\n    eventIds\n    listingIds\n    owner {\n      id\n      name\n      slug\n    }\n  }\n}",
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-membership?${params}`, {
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
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query GetMembership($membershipId: ID!) {\n  membership(id: $membershipId) {\n    id\n    organizationName\n    state\n    allEvents\n    eventIds\n    listingIds\n    owner {\n      id\n      name\n      slug\n    }\n  }\n}`. |
| `variables` | object | yes | Optional GraphQL variables object for the membership query. Default: `{"membershipId":"69bd3f0c22b4d6003c5b58f6"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-membership.md) for the provider-specific parameters and requirements.

