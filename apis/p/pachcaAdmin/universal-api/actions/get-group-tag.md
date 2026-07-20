# Pachca (Admin): Get Group Tag

Retrieves a group tag from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-group-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-group-tag?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-group-tag?${params}`, {
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
| `id` | number | yes | The Pachca group tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "name": "Ava Chen",
        "usersCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.usersCount` | number |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /group_tags/:id` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-tag.md) for the provider-specific parameters and requirements.

