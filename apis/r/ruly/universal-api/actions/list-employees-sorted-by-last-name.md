# Ruly: List Employees Sorted by Last Name



```
GET https://connect.mindcloud.co/v1/universal/ruly/latest/actions/list-employees-sorted-by-last-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ruly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ruly/latest/actions/list-employees-sorted-by-last-name?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ruly/latest/actions/list-employees-sorted-by-last-name?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ruly API returns.

## Native endpoint

Through the native Ruly API, this operation is `GET data/employee/` (base URL `https://mindcloud.api.rulyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees-sorted-by-last-name.md) for the provider-specific parameters and requirements.

