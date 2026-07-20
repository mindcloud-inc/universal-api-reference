# Missive: Search Messages by Email Message ID

Finds Missive messages by email message ID.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/search-messages-by-email-message-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/search-messages-by-email-message-id?connectionId=$CONNECTION_ID&emailMessageId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailMessageId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/search-messages-by-email-message-id?${params}`, {
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
| `emailMessageId` | string | yes | Email Message-ID header value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Missive API returns.

## Native endpoint

Through the native Missive API, this operation is `GET /messages` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-messages-by-email-message-id.md) for the provider-specific parameters and requirements.

