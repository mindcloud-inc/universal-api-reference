# Bridgit Bench: Get Account Integration



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-account-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-account-integration?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&view=All" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "view": "All"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-account-integration?${params}`, {
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
| `accountId` | number | yes | The account ID (must be greater than zero). |
| `view` | list<string> | yes | Which slice to return: `all` (whole marketplace) or `mine` (the account's integrations and enabled products). One of: `All`, `Mine`. |
| `search` | string | no | Optional free-text search over the integration name. |
| `objectTypes` | list<string> | no | Optional object-type filter (comma-delimited): people / projects / opportunities. Matches integrations exposing any of the given types. One of: `Opportunities`, `People`, `Projects`. Accepts multiple values in one string, delimited by `,`. |
| `connectionStatus` | list<string> | no | Optional filter: connected / disconnected. One of: `Connected`, `Disconnected`, `ReadyToConnect`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/integrations` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-account-integration.md) for the provider-specific parameters and requirements.

