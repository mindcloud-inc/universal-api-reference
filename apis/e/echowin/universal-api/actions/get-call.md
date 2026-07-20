# echowin: Get Call

Retrieves a call from echowin.

```
GET https://connect.mindcloud.co/v1/universal/echowin/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a echowin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/get-call?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/echowin/latest/actions/get-call?${params}`, {
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
| `callId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native echowin API returns.

## Native endpoint

Through the native echowin API, this operation is `GET /calls/:callId` (base URL `https://echo.win/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

