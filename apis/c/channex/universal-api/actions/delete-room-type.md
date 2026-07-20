# Channex: Delete Room Type

Deletes a room type from Channex.

```
DELETE https://connect.mindcloud.co/v1/universal/channex/latest/actions/delete-room-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/channex/latest/actions/delete-room-type?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/delete-room-type?${params}`, {
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
| `id` | string | yes | UUID of the room type to delete. |
| `force` | boolean | no | Set true to force removal when supported by Channex. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.message` | string |  |

## Native endpoint

Through the native Channex API, this operation is `DELETE /room_types/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-room-type.md) for the provider-specific parameters and requirements.

