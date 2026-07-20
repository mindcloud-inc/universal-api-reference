# Weberlo: List Visitors

Retrieves a list of visitors from Weberlo.

```
GET https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-visitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-visitors?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=2026-04-01T00%3A00%3A00Z&endDate=2026-04-03T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "2026-04-01T00:00:00Z",
  "endDate": "2026-04-03T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-visitors?${params}`, {
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
| `startDate` | string | yes | Start of the visitor search window. Example: `2026-04-01T00:00:00Z`. |
| `endDate` | string | yes | End of the visitor search window. Example: `2026-04-03T00:00:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weberlo API returns.

## Native endpoint

Through the native Weberlo API, this operation is `POST /visitor/list` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-visitors.md) for the provider-specific parameters and requirements.

