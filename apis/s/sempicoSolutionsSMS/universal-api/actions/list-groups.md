# Sempico Solutions SMS: List Groups



```
GET https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/list-groups?${params}`, {
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
| `limit` | number | no | Number of groups to return. Default: `10`. |
| `offset` | number | no | Page offset for group listing. Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id_group` | number | no | Optional group ID to return one specific group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupDetails": {
        "countAll": 1,
        "countResult": 1,
        "limit": 1,
        "offset": 1
      },
      "list": {
        "id_group": 1,
        "name_group": "Ava Chen",
        "numbers_count": 1,
        "on_birth": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupDetails.countAll` | number | Total matching groups. |
| `groupDetails.countResult` | number | Number of groups returned. |
| `groupDetails.limit` | number | Requested limit. |
| `groupDetails.offset` | number | Requested offset. |
| `list` | array<object> | Group records. |
| `list.id_group` | number | Group ID. |
| `list.name_group` | string | Group name. |
| `list.numbers_count` | number | Number of phone numbers in the group. |
| `list.on_birth` | boolean | Whether birthday greetings are enabled. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /group` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

