# EasyPost: Get Address

Retrieves details for an address from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-address?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-address?${params}`, {
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
| `id` | string | yes | EasyPost Address ID, beginning with adr_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "company": "string",
      "country": "string",
      "email": "ava@example.com",
      "id": "string",
      "mode": "string",
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "state": "string",
      "street1": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City. |
| `company` | string | Company name. |
| `country` | string | Country. |
| `email` | string | Email address. |
| `id` | string | EasyPost Address ID. |
| `mode` | string | EasyPost mode. |
| `name` | string | Recipient or sender name. |
| `object` | string | EasyPost object type. |
| `phone` | string | Phone number. |
| `state` | string | State. |
| `street1` | string | Street address. |
| `zip` | string | Postal code. |

## Native endpoint

Through the native EasyPost API, this operation is `GET /addresses/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address.md) for the provider-specific parameters and requirements.

