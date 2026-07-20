# Twilio: Delete Messaging Service

Deletes an existing messaging service from Twilio.

```
DELETE https://connect.mindcloud.co/v1/universal/twilio/latest/actions/delete-messaging-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/delete-messaging-service?connectionId=$CONNECTION_ID&sid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/delete-messaging-service?${params}`, {
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
| `sid` | string | yes | Messaging Service SID to delete |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Twilio API returns.

## Native endpoint

Through the native Twilio API, this operation is `DELETE https://messaging.twilio.com/v1/Services/:Sid` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-messaging-service.md) for the provider-specific parameters and requirements.

