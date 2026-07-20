# Geocodio: Delete Geocoding List

Deletes an existing geocoding list from Geocodio.

```
DELETE https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/delete-geocoding-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/delete-geocoding-list?connectionId=$CONNECTION_ID&id=42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/delete-geocoding-list?${params}`, {
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
| `id` | number | yes | Geocodio list ID. Example: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the list was deleted successfully. |

## Native endpoint

Through the native Geocodio API, this operation is `DELETE /lists/{id}` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-geocoding-list.md) for the provider-specific parameters and requirements.

