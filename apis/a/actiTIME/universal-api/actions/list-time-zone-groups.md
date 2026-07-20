# actiTIME: List Time Zone Groups

Retrieves time zone groups from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-time-zone-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-time-zone-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-time-zone-groups?${params}`, {
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
| `name` | string | no | Exact time zone group name match, case-insensitive. |
| `sort` | string | no | Sorting tokens like +name or -name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default": true,
      "id": 1,
      "name": "Ava Chen",
      "timeZoneId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean | Whether the time zone group is the default. |
| `id` | number | Unique time zone group identifier. |
| `name` | string | Time zone group name. |
| `timeZoneId` | string | IANA time zone identifier. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /timeZoneGroups` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-zone-groups.md) for the provider-specific parameters and requirements.

