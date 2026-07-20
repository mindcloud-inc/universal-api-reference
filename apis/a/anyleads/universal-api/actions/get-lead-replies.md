# Anyleads: Get Lead Replies

Retrieves replies for a lead from Anyleads.

```
GET https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/get-lead-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anyleads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/get-lead-replies?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/get-lead-replies?${params}`, {
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
| `email` | string | yes | Lead email address whose replies should be fetched. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anyleads API returns.

## Native endpoint

Through the native Anyleads API, this operation is `POST /api-product/incoming-webhook/fetch-replies-from-single-lead` (base URL `https://myapiconnect.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-replies.md) for the provider-specific parameters and requirements.

