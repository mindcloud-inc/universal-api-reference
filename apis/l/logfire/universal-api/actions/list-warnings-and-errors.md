# Logfire: List Warnings And Errors

Retrieves warnings and errors from Logfire.

```
GET https://connect.mindcloud.co/v1/universal/logfire/latest/actions/list-warnings-and-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logfire/latest/actions/list-warnings-and-errors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logfire/latest/actions/list-warnings-and-errors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logfire API returns.

## Native endpoint

Through the native Logfire API, this operation is `GET /v1/query` (base URL `https://logfire-api.pydantic.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-warnings-and-errors.md) for the provider-specific parameters and requirements.

