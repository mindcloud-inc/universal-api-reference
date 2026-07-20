# Novofon: Request Call Recording

Retrieves call recording links from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-call-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-call-recording?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/request-call-recording?${params}`, {
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
| `callId` | string | no | Unique call ID from the statistics response. |
| `lifetime` | string | no | Optional link lifetime in seconds. Docs say minimum 180, maximum 5184000, default 1800. |
| `pbxCallId` | string | no | Persistent PBX call ID that can return multiple recording links. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Novofon API returns.

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/pbx/record/request/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-call-recording.md) for the provider-specific parameters and requirements.

