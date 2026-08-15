# Samsara: Get Vehicle Stats



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-vehicle-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-vehicle-stats?connectionId=$CONNECTION_ID&limit=25&offset=0&types%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "types[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-vehicle-stats?${params}`, {
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
| `types[]` | array<string> | yes | Vehicle statistic types to return; up to three types. |
| `time` | string | no | Return the latest statistics at or before this RFC 3339 timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samsara API returns.

## Native endpoint

Through the native Samsara API, this operation is `GET fleet/vehicles/stats` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-vehicle-stats.md) for the provider-specific parameters and requirements.

