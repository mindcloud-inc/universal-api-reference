# Grand Avenue Software: Get Training Record

Retrieves a training record from Grand Avenue Software by ID.

```
GET https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-training-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grand Avenue Software `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-training-record?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-training-record?${params}`, {
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
| `select` | list<string> | no | Accepts multiple values in one string. |
| `expand` | list<string> | no | Accepts multiple values in one string. |
| `id` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Grand Avenue Software API returns.

## Native endpoint

Through the native Grand Avenue Software API, this operation is `GET /TrainingRecords/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-training-record.md) for the provider-specific parameters and requirements.

