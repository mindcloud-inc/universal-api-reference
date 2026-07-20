# Persona: List User Audit Logs



```
GET https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-user-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Persona `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-user-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-user-audit-logs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Persona API returns.

## Native endpoint

Through the native Persona API, this operation is `GET /user-audit-logs` (base URL `https://api.withpersona.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-audit-logs.md) for the provider-specific parameters and requirements.

