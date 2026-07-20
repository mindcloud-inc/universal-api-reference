# Wasi: Create Client

Creates a new client in Wasi.

```
POST https://connect.mindcloud.co/v1/universal/wasi/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasi/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "id_client": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_client` | number | Created Wasi client identifier. |
| `status` | string | Wasi operation status. |

## Native endpoint

Through the native Wasi API, this operation is `POST /client/add` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

