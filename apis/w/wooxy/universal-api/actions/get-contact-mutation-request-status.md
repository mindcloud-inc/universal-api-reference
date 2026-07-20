# Wooxy: Get Contact Mutation Request Status

Retrieves contact mutation request statuses from Wooxy.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-contact-mutation-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-contact-mutation-request-status?connectionId=$CONNECTION_ID&ids%5B%5D=requestId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "requestId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-contact-mutation-request-status?${params}`, {
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
| `ids[]` | array<string> | yes | Array of Wooxy contact mutation request IDs. Example: `requestId`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wooxy API returns.

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/request/find` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-mutation-request-status.md) for the provider-specific parameters and requirements.

