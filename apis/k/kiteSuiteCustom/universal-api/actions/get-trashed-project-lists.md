# Kite Suite: Get trashed project lists.



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-trashed-project-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-trashed-project-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-trashed-project-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/project/trashed` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trashed-project-lists.md) for the provider-specific parameters and requirements.

