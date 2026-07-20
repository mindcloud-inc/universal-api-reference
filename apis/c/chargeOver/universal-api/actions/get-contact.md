# ChargeOver: Get Contact

Retrieves detailed contact records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-contact?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-contact?${params}`, {
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
| `userId` | number | yes | The ChargeOver contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer_id": 1,
      "email": "ava@example.com",
      "mobile": "string",
      "name": "Ava Chen",
      "phone": "string",
      "url_self": "https://example.com",
      "user_id": 1,
      "user_type_name": "Ava Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer_id` | number |  |
| `email` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `url_self` | string |  |
| `user_id` | number |  |
| `user_type_name` | string |  |
| `username` | string |  |

## Native endpoint

Through the native ChargeOver API, this operation is `GET /user/:user_id` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

