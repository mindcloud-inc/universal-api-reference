# actiTIME: List Leave Types

Retrieves a list of leave types from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-leave-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-leave-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-leave-types?${params}`, {
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
| `archived` | boolean | no | Filter archived vs active leave types. |
| `balance` | string | no | Balance filter value. |
| `ids` | string | no | Comma-separated leave type ids to be returned. |
| `name` | string | no | Exact leave type name match, case-insensitive. |
| `sort` | string | no | Sorting tokens like +name or -name. |
| `words` | string | no | Return leave types containing all given words in the name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "balance": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the leave type is archived. |
| `balance` | string | Balance affected by this leave type. |
| `id` | number | Unique leave type identifier. |
| `name` | string | Leave type name. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /leaveTypes` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leave-types.md) for the provider-specific parameters and requirements.

