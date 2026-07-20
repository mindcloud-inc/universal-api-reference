# Starfish: Delete Accommodation

Deletes an existing accommodation from Starfish.

```
DELETE https://connect.mindcloud.co/v1/universal/starfish/latest/actions/delete-accommodation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/delete-accommodation?connectionId=$CONNECTION_ID&accommodationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accommodationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/delete-accommodation?${params}`, {
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
| `accommodationId` | number | yes | Accommodation ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Starfish API returns.

## Native endpoint

Through the native Starfish API, this operation is `DELETE /accommodations/:accommodation_id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-accommodation.md) for the provider-specific parameters and requirements.

