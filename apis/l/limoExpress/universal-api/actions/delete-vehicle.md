# LimoExpress: Delete Vehicle

Deletes an existing vehicle from LimoExpress.

```
DELETE https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/delete-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/delete-vehicle?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/delete-vehicle?${params}`, {
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
| `id` | string | yes | Identifier of the vehicle to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Operation payload when returned by the API. |
| `message` | string | Operation status or error message. |
| `success` | boolean | Operation success flag when provided by the API. |

## Native endpoint

Through the native LimoExpress API, this operation is `DELETE /api/integration/vehicles` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vehicle.md) for the provider-specific parameters and requirements.

