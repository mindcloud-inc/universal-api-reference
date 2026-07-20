# Wasi: Remove Client Property Link

Deletes a client-to-property relationship from Wasi.

```
DELETE https://connect.mindcloud.co/v1/universal/wasi/latest/actions/remove-client-property-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/remove-client-property-link?connectionId=$CONNECTION_ID&client_id=1&property_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "client_id": "1",
  "property_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/remove-client-property-link?${params}`, {
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
| `client_id` | number | yes | Wasi client ID. Default: `1`. |
| `property_id` | number | yes | Wasi property ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Wasi operation status. |

## Native endpoint

Through the native Wasi API, this operation is `POST /client/:id_client/remove-property/:id_property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-client-property-link.md) for the provider-specific parameters and requirements.

