# Bridgit Bench: List Account Person Field Values



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-person-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-person-field-values?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-person-field-values?${params}`, {
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
| `id` | number | yes | The Account ID |
| `state` | list<string> | no | If specified and non-zero, only include field vlaues for people matching the given state. The available values are defined as follows: - active: include only Active people - deactivated: include only Deactivated people - all: include all people, regardless of state One of: `Active`, `All`, `Deactivated`. Default: `Active`. |
| `personIds` | number | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Accepts multiple values in one string, delimited by `,`. |
| `employeeId` | string | no | Optional - for filtering result by system field "Employee ID" |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeEmpty` | boolean | no | If true, the response will include all person field values, even if no value is set for a given field. If false, field values that are empty are not included in the response. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/Accounts/:id/person-field-values` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-person-field-values.md) for the provider-specific parameters and requirements.

