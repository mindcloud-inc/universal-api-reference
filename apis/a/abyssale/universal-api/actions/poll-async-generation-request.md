# Abyssale: Poll Async Generation Request

Retrieves an async generation request status from Abyssale.

```
GET https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/poll-async-generation-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abyssale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/poll-async-generation-request?connectionId=$CONNECTION_ID&generation_request_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generation_request_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/poll-async-generation-request?${params}`, {
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
| `generation_request_id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abyssale API returns.

## Native endpoint

Through the native Abyssale API, this operation is `GET /generation-request/:generation_request_id` (base URL `https://api.abyssale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/poll-async-generation-request.md) for the provider-specific parameters and requirements.

