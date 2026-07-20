# BoxHero: Get Partner

Retrieves a partner from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-partner?connectionId=$CONNECTION_ID&partnerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partnerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-partner?${params}`, {
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
| `partnerId` | number | yes | Unique identifier for the partner |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "address": "string",
        "email": "ava@example.com",
        "id": 1,
        "memo": "string",
        "name": "Ava Chen",
        "phone": "string",
        "type": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item.address` | string |  |
| `item.email` | string |  |
| `item.id` | number |  |
| `item.memo` | string |  |
| `item.name` | string |  |
| `item.phone` | string |  |
| `item.type` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/partners/:partner_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-partner.md) for the provider-specific parameters and requirements.

