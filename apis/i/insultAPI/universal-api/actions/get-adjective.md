# Insult API: Get Adjective



```
GET https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-adjective
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insult API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-adjective?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-adjective?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Insult API API returns.

## Native endpoint

Through the native Insult API API, this operation is `GET /adjective` (base URL `https://insult.mattbas.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-adjective.md) for the provider-specific parameters and requirements.

