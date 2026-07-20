# Makeswift: Delete Route



```
DELETE https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/delete-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/delete-route?connectionId=$CONNECTION_ID&routeIdOrPathname=Ava%20Chen&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "routeIdOrPathname": "Ava Chen",
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/delete-route?${params}`, {
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
| `routeIdOrPathname` | string | yes | Route ID or pathname to delete. |
| `siteId` | string | yes | The site ID containing the route. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Makeswift API returns.

## Native endpoint

Through the native Makeswift API, this operation is `DELETE /v2/routes/:routeIdOrPathname` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-route.md) for the provider-specific parameters and requirements.

