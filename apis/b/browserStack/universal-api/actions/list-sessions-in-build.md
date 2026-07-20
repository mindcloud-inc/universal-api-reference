# BrowserStack: List Sessions In Build

Retrieves build session records from BrowserStack Automate.

```
GET https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/list-sessions-in-build
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/list-sessions-in-build?connectionId=$CONNECTION_ID&buildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "buildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/list-sessions-in-build?${params}`, {
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
| `buildId` | string | yes | BrowserStack build hashed ID from List Builds. |
| `limit` | number | no | Maximum number of sessions to return. |
| `offset` | number | no | Offset for session list pagination. |
| `status` | string | no | Session status filter: running, done, timeout, or failed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BrowserStack API returns.

## Native endpoint

Through the native BrowserStack API, this operation is `GET /automate/builds/:build_id/sessions.json` (base URL `https://api.browserstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions-in-build.md) for the provider-specific parameters and requirements.

