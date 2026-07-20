# FTrack: Query Schemas

Retrieves entity schemas from FTrack.

```
GET https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/query-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/query-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/query-schemas?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-schemas.md) for the provider-specific parameters and requirements.

