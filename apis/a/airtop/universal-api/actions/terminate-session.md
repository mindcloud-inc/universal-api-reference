# Airtop: Terminate Session

Terminates an existing session in Airtop.

```
DELETE https://connect.mindcloud.co/v1/universal/airtop/latest/actions/terminate-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/terminate-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtop/latest/actions/terminate-session?${params}`, {
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
| `sessionId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airtop API returns.

## Native endpoint

Through the native Airtop API, this operation is `DELETE /sessions/:sessionId` (base URL `https://api.airtop.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/terminate-session.md) for the provider-specific parameters and requirements.

