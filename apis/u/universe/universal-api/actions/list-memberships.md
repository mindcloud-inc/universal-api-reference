# Universe: List Memberships

Retrieves memberships for the authenticated viewer in Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-memberships?connectionId=$CONNECTION_ID&query=query%20ListMemberships%20%7B%0A%20%20viewer%20%7B%0A%20%20%20%20id%0A%20%20%20%20memberships%20%7B%0A%20%20%20%20%20%20nodes%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20organizationName%0A%20%20%20%20%20%20%20%20state%0A%20%20%20%20%20%20%20%20allEvents%0A%20%20%20%20%20%20%20%20owner%20%7B%0A%20%20%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20%20%20name%0A%20%20%20%20%20%20%20%20%20%20slug%0A%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListMemberships {\n  viewer {\n    id\n    memberships {\n      nodes {\n        id\n        organizationName\n        state\n        allEvents\n        owner {\n          id\n          name\n          slug\n        }\n      }\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-memberships?${params}`, {
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
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is a membership-focused example for this action. Default: `query ListMemberships {\n  viewer {\n    id\n    memberships {\n      nodes {\n        id\n        organizationName\n        state\n        allEvents\n        owner {\n          id\n          name\n          slug\n        }\n      }\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default memberships query. Default: `{}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memberships.md) for the provider-specific parameters and requirements.

