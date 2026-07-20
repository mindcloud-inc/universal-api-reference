# actiTIME: List Types of Work

Retrieves a list of types of work from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-types-of-work
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-types-of-work?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-types-of-work?${params}`, {
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
| `archived` | boolean | no | Filter archived vs active types of work. |
| `billable` | boolean | no | Filter billable vs non-billable types of work. |
| `ids` | string | no | Comma-separated type of work ids to return. |
| `name` | string | no | Exact type of work name match, case-insensitive. |
| `sort` | string | no | Sorting tokens like +name or -name. |
| `words` | string | no | Return types of work containing all given words in the name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billable": true,
      "default": true,
      "id": 1,
      "name": "Ava Chen",
      "rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the type of work is archived. |
| `billable` | boolean | Whether the type of work is billable. |
| `default` | boolean | Whether the type of work is the default option. |
| `id` | number | Unique type of work identifier. |
| `name` | string | Type of work name. |
| `rate` | number | Hourly rate for the type of work. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /typesOfWork` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-types-of-work.md) for the provider-specific parameters and requirements.

