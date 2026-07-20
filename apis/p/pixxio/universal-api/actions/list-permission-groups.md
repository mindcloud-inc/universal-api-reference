# pixx.io: List Permission Groups

Retrieves permission groups from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-permission-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-permission-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-permission-groups?${params}`, {
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
| `isAdmin` | boolean | no | Filter admin permission groups. |
| `isExternal` | boolean | no | Filter external permission groups. |
| `isReadOnly` | boolean | no | Filter read-only permission groups. |
| `searchTerm` | string | no | Search permission groups by term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permissionGroups": {
        "id": 1,
        "name": "Ava Chen"
      },
      "quantity": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permissionGroups` | array<object> |  |
| `permissionGroups.id` | number |  |
| `permissionGroups.name` | string |  |
| `quantity` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /permissionGroups` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-permission-groups.md) for the provider-specific parameters and requirements.

