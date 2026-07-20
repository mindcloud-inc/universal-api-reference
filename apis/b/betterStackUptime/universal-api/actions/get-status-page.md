# Better Stack Uptime: Get Status Page

Retrieves a status page from Better Stack Uptime.

```
GET https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-status-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-status-page?connectionId=$CONNECTION_ID&statusPageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statusPageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-status-page?${params}`, {
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
| `statusPageId` | string | yes | Status page ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `GET /v2/status-pages/:statusPageId` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status-page.md) for the provider-specific parameters and requirements.

