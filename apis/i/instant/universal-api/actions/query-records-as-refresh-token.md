# Instant: Query Records As Refresh Token

Retrieves records from Instant as a user by refresh token.

```
GET https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records-as-refresh-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records-as-refresh-token?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D&asToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]",
  "asToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records-as-refresh-token?${params}`, {
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
| `query` | object | yes | InstaQL query object to run. |
| `asToken` | string | yes | Refresh token to impersonate for permission-aware queries. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Instant API returns.

## Native endpoint

Through the native Instant API, this operation is `POST /admin/query` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-records-as-refresh-token.md) for the provider-specific parameters and requirements.

