# HoorayHR: List Employment Term Assignments

Retrieves employment term assignments from HoorayHR.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-employment-term-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-employment-term-assignments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-employment-term-assignments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HoorayHR API returns.

## Native endpoint

Through the native HoorayHR API, this operation is `GET /employment-term-assignments` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employment-term-assignments.md) for the provider-specific parameters and requirements.

