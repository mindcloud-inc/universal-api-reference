# Wasi: Update Client

Updates an existing client in Wasi.

```
PUT https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client_id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasi/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client_id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Client address. |
| `birthday` | date | no | Client birthday. |
| `cell_phone` | string | no | Client mobile phone number. |
| `city_id` | number | no | Client city ID. |
| `client_id` | number | yes | Wasi client ID to update. Default: `1`. |
| `client_origin_id` | number | no | Client origin ID. |
| `client_status_id` | number | no | Client status ID. |
| `client_type_id` | number | no | Primary client type ID. |
| `comment` | string | no | Client comment. |
| `country_id` | number | no | Client country ID. |
| `email` | string | no | Client email address. |
| `first_name` | string | no | Client first name. |
| `identification` | string | no | Client identification number. |
| `last_name` | string | no | Client last name. |
| `phone` | string | no | Client phone number. |
| `reference` | string | no | Client reference. |
| `region_id` | number | no | Client region ID. |
| `send_information` | boolean | no | Whether the client accepts information messages. |
| `user_id` | number | no | Assigned Wasi user ID. |

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

Through the native Wasi API, this operation is `POST /client/update/:id_client` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

