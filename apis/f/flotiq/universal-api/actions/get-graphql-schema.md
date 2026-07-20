# Flotiq: Get GraphQL Schema

Retrieves the GraphQL schema from Flotiq.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-graphql-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-graphql-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-graphql-schema?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flotiq API returns.

## Native endpoint

Through the native Flotiq API, this operation is `GET https://api.flotiq.com/api/v2/graphql/schema` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-graphql-schema.md) for the provider-specific parameters and requirements.

