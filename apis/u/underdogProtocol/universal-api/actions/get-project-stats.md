# Underdog Protocol: Get Project Stats

Retrieves project stats from Underdog Protocol.

```
GET https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/get-project-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Underdog Protocol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/get-project-stats?connectionId=$CONNECTION_ID&transferable=n&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transferable": "n",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/get-project-stats?${params}`, {
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
| `transferable` | list | yes | Value must be either 't' for transferable or 'n' for non-transferable One of: `n`, `t`. |
| `projectId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Underdog Protocol API returns.

## Native endpoint

Through the native Underdog Protocol API, this operation is `GET /v2/projects/:transferable/:projectId/stats` (base URL `https://dev.underdogprotocol.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-stats.md) for the provider-specific parameters and requirements.

