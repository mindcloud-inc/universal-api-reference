# EenvoudigFactureren: Get Client

Retrieves a client from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-client?connectionId=$CONNECTION_ID&client_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "client_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-client?${params}`, {
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
| `client_id` | string | yes | EenvoudigFactureren client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "client_id": 1,
      "country": "string",
      "email_address": "ava@example.com",
      "last_activity": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": "string",
      "phone_number": "string",
      "postal_code": "string",
      "state": "string",
      "street": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `client_id` | number |  |
| `country` | string |  |
| `email_address` | string |  |
| `last_activity` | date |  |
| `name` | string |  |
| `number` | string |  |
| `phone_number` | string |  |
| `postal_code` | string |  |
| `state` | string |  |
| `street` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /clients/:client_id` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

