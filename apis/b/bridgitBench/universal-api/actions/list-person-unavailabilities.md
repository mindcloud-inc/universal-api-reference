# Bridgit Bench: List Person Unavailabilities



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-unavailabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-unavailabilities?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-unavailabilities?${params}`, {
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
| `accountId` | number | yes | The Account ID |
| `id` | number | yes | Id of the person to get unavailabilities for |
| `start` | date | no | Date from which to start the range (Default: 0001-01-01) |
| `end` | date | no | Date from which to end the range (Default: 9999-12-31) |
| `sortOrder` | list<string> | no | The order to return unavailabilities. Default is StartDateAscending One of: `EndDateDescending`, `StartDateAscending`. Default: `StartDateAscending`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/persons/:id/unavailabilities` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-unavailabilities.md) for the provider-specific parameters and requirements.

