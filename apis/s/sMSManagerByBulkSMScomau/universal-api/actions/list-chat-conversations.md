# SMS Manager by BulkSMS.com.au: List Chat Conversations



```
GET https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/list-chat-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Manager by BulkSMS.com.au `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/list-chat-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/list-chat-conversations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS Manager by BulkSMS.com.au API returns.

## Native endpoint

Through the native SMS Manager by BulkSMS.com.au API, this operation is `GET /chats` (base URL `https://smsmanager.com.au/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-conversations.md) for the provider-specific parameters and requirements.

