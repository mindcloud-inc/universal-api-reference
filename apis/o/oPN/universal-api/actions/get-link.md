# OPN: Get Link

Retrieves details for a link from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-link?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-link?${params}`, {
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
| `id` | string | yes | The link ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "charges": {},
      "created_at": "string",
      "currency": "string",
      "deleted": true,
      "deleted_at": "string",
      "description": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "multiple": true,
      "object": "string",
      "payment_uri": "string",
      "title": "string",
      "used": true,
      "used_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `charges` | object |  |
| `created_at` | string |  |
| `currency` | string |  |
| `deleted` | boolean |  |
| `deleted_at` | string |  |
| `description` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `multiple` | boolean |  |
| `object` | string |  |
| `payment_uri` | string |  |
| `title` | string |  |
| `used` | boolean |  |
| `used_at` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /links/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

