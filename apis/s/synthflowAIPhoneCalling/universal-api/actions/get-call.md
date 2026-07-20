# Synthflow AI Phone Calling: Get Call

Retrieves a phone call from Synthflow.

```
GET https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synthflow AI Phone Calling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-call?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-call?${params}`, {
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
| `callId` | string | yes | The Synthflow call identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Synthflow AI Phone Calling API returns.

## Native endpoint

Through the native Synthflow AI Phone Calling API, this operation is `GET /calls/:call_id` (base URL `https://api.synthflow.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

