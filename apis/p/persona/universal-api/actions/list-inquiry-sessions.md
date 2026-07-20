# Persona: List Inquiry Sessions



```
GET https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-inquiry-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Persona `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-inquiry-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-inquiry-sessions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Persona API returns.

## Native endpoint

Through the native Persona API, this operation is `GET /inquiry-sessions` (base URL `https://api.withpersona.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inquiry-sessions.md) for the provider-specific parameters and requirements.

