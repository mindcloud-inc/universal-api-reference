# Pachca (Admin): List Group Tags

Retrieves group tags from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-group-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-group-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-group-tags?${params}`, {
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
| `names[]` | array<string> | no |  |
| `limit` | number | no |  |
| `cursor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": 1,
          "name": "Ava Chen",
          "usersCount": 1
        }
      ],
      "meta": {
        "paginate": {
          "nextPage": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].id` | number |  |
| `data[].name` | string |  |
| `data[].usersCount` | number |  |
| `meta.paginate.nextPage` | string |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /group_tags` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-tags.md) for the provider-specific parameters and requirements.

