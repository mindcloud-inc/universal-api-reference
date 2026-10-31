# Bridgit Bench: List Person Attachments



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-attachments?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&personId=1" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-attachments?${params}`, {
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
| `state` | list<string> | no | The state of the attachment for filter One of: `All`, `Completed`, `Failed`, `InProgress`. Default: `Completed`. |
| `creatorId` | number | no | The ID of attachment creator for filter |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/persons/:personId/attachments` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-attachments.md) for the provider-specific parameters and requirements.

