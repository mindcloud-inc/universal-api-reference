# Restoplace: List Item Types

Retrieves item types from Restoplace.

```
GET https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/list-item-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/list-item-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/list-item-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `GET /itemTypes` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-item-types.md) for the provider-specific parameters and requirements.

