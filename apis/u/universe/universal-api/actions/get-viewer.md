# Universe: Get Viewer

Retrieves the authenticated viewer from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-viewer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-viewer?connectionId=$CONNECTION_ID&query=query%20%7B%20viewer%20%7B%20id%20firstName%20lastName%20memberships%20%7B%20nodes%20%7B%20id%20owner%20%7B%20id%20name%20%7D%20%7D%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { viewer { id firstName lastName memberships { nodes { id owner { id name } } } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-viewer?${params}`, {
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
| `query` | string | yes | Default read-only viewer query used to validate the authenticated Universe connection and inspect memberships. Default: `query GetViewer {\n  viewer {\n    id\n    firstName\n    lastName\n    email\n    host\n    memberships {\n      nodes {\n        id\n        organizationName\n        owner {\n          id\n          name\n          slug\n        }\n      }\n    }\n  }\n}`. Example: `query { viewer { id firstName lastName memberships { nodes { id owner { id name } } } } }`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default viewer query. Default: `{}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-viewer.md) for the provider-specific parameters and requirements.

