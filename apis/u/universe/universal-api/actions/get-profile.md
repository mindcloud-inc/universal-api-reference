# Universe: Get Profile

Retrieves a specific profile from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-profile?connectionId=$CONNECTION_ID&query=query%20GetProfile(%24profileId%3A%20ID!)%20%7B%0A%20%20profile(id%3A%20%24profileId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20name%0A%20%20%20%20slug%0A%20%20%20%20url%0A%20%20%20%20locale%0A%20%20%20%20host%0A%20%20%20%20isBusinessSeller%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetProfile($profileId: ID!) {\n  profile(id: $profileId) {\n    id\n    name\n    slug\n    url\n    locale\n    host\n    isBusinessSeller\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-profile?${params}`, {
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
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query GetProfile($profileId: ID!) {\n  profile(id: $profileId) {\n    id\n    name\n    slug\n    url\n    locale\n    host\n    isBusinessSeller\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables object for the profile query. Default: `{"profileId":"69bc5b60b86a1d003cef1424"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

