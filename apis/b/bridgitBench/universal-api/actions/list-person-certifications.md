# Bridgit Bench: List Person Certifications



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-certifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-certifications?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&personId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "personId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-certifications?${params}`, {
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
| `personId` | number | yes | The Person ID |
| `ids` | number | no | (Optional) Filters the result to contain person certifications that match the ids passed in. Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/persons/:personId/certifications` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-certifications.md) for the provider-specific parameters and requirements.

