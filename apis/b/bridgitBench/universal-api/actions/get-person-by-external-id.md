# Bridgit Bench: Get Person by External ID



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-person-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-person-by-external-id?connectionId=$CONNECTION_ID&accountId=1&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-person-by-external-id?${params}`, {
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
| `accountId` | number | yes |  |
| `externalId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/external/persons/:externalId` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-by-external-id.md) for the provider-specific parameters and requirements.

