# pixx.io: Get Permission Group

Retrieves a permission group from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-permission-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-permission-group?connectionId=$CONNECTION_ID&permissionGroupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permissionGroupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-permission-group?${params}`, {
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
| `permissionGroupId` | number | yes | The pixx.io permission group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permissionGroup": {
        "id": 1,
        "name": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permissionGroup` | object |  |
| `permissionGroup.id` | number |  |
| `permissionGroup.name` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /permissionGroups/:permission_group_id` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-permission-group.md) for the provider-specific parameters and requirements.

