# CallPage: Get Call

Retrieves a single call from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-call?connectionId=$CONNECTION_ID&callId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-call?${params}`, {
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
| `callId` | number | yes | The call identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "call": {
          "data": {
            "id": 1,
            "sid": "string"
          }
        },
        "cancelled_at": "string",
        "created_at": "string",
        "human_status": "string",
        "id": 1,
        "leadable_description": "string",
        "scheduled_at": "string",
        "to": "string",
        "to_formatted": "string"
      },
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.call.data.id` | number | The nested call attempt identifier. |
| `data.call.data.sid` | string | The provider call SID. |
| `data.cancelled_at` | string | When the call was cancelled, if applicable. |
| `data.created_at` | string | When the call request was created. |
| `data.human_status` | string | The human-readable call status. |
| `data.id` | number | The call identifier. |
| `data.leadable_description` | string | The leadable description. |
| `data.scheduled_at` | string | When the call is scheduled, if applicable. |
| `data.to` | string | The destination phone number. |
| `data.to_formatted` | string | The formatted destination phone number. |
| `id` | number | The top-level call record identifier. |

## Native endpoint

Through the native CallPage API, this operation is `GET https://core.callpage.io/api/v3/external/calls/{call_id}` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

