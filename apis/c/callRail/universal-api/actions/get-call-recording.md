# CallRail: Get Call Recording

Retrieves a call recording from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/get-call-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/get-call-recording?connectionId=$CONNECTION_ID&account_id=string&call_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string",
  "call_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/get-call-recording?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |
| `call_id` | string | yes | The CallRail call ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/calls/:call_id/recording.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-recording.md) for the provider-specific parameters and requirements.

