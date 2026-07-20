# Webex Interact: Retrieve scheduled SMS request

Finds a scheduled SMS request in Webex Interact by ID.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-scheduled-sms-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-scheduled-sms-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-scheduled-sms-request?${params}`, {
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
| `id` | string | yes | Scheduled SMS request ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message_body": "string",
      "name": "Ava Chen",
      "request_type": "string",
      "scheduled_at": "2026-05-07T12:00:00.000Z",
      "sender_name": "Ava Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Scheduled request ID. |
| `message_body` | string | Scheduled SMS message body. |
| `name` | string | Scheduled request name. |
| `request_type` | string | Request type returned by the API. |
| `scheduled_at` | date | Scheduled send time. |
| `sender_name` | string | Sender name used for the scheduled request. |
| `status` | string | Scheduled request status. |
| `type` | string | Scheduled request type. |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /campaigns/v1/scheduled` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-scheduled-sms-request.md) for the provider-specific parameters and requirements.

