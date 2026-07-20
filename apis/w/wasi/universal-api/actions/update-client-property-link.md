# Wasi: Update Client Property Link

Updates a client-to-property relationship in Wasi.

```
PUT https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-client-property-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-client-property-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client_id": "1",
  "client_type_id": "1",
  "property_id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-client-property-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client_id": "1",
    "client_type_id": "1",
    "property_id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client_id` | number | yes | Wasi client ID. Default: `1`. |
| `client_type_id` | number | yes | Updated relationship client type ID. Default: `1`. |
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

Through the native Wasi API, this operation is `POST /client/:id_client/update-property/:id_property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client-property-link.md) for the provider-specific parameters and requirements.

