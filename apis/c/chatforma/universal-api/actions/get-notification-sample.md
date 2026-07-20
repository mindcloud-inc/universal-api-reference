# Chatforma: Get Notification Sample

Retrieves notification sample fields from Chatforma.

```
GET https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/get-notification-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/get-notification-sample?connectionId=$CONNECTION_ID&botId=1&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1",
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/get-notification-sample?${params}`, {
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
| `botId` | number | yes | Bot ID to get a notification sample for |
| `formId` | string | yes | Form ID to get a notification sample for |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatforma API returns.

## Native endpoint

Through the native Chatforma API, this operation is `GET /notification-sample` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-sample.md) for the provider-specific parameters and requirements.

