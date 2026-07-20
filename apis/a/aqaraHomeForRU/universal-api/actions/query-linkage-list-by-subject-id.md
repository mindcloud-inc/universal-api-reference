# Aqara Home for RU: List Linkages by Subject

Retrieves linkages by subject from Aqara Home for RU.

```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/query-linkage-list-by-subject-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for RU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/query-linkage-list-by-subject-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/query-linkage-list-by-subject-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aqara Home for RU API returns.

## Native endpoint

Through the native Aqara Home for RU API, this operation is `POST /v3.0/open/api` (base URL `https://open-ru.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-linkage-list-by-subject-id.md) for the provider-specific parameters and requirements.

