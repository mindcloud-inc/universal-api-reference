# Airmeet: Delete Session

Deletes an existing session from Airmeet.

```
DELETE https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/delete-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/delete-session?connectionId=$CONNECTION_ID&airmeetId=string&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "airmeetId": "string",
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/delete-session?${params}`, {
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
| `airmeetId` | string | yes | The Airmeet event ID. |
| `sessionId` | string | yes | The session ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `DELETE /airmeet/{airmeetId}/session/{sessionId}` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session.md) for the provider-specific parameters and requirements.

