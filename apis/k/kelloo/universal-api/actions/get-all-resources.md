# Kelloo: Get All Resources

Retrieves all resource records from Kelloo.

```
GET https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-all-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kelloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-all-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-all-resources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kelloo API returns.

## Native endpoint

Through the native Kelloo API, this operation is `GET /Resource` (base URL `https://plan.kelloo.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-resources.md) for the provider-specific parameters and requirements.

