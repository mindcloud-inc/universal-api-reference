# Monica CRM: Get Gift

Retrieves a gift from Monica CRM.

```
GET https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-gift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-gift?connectionId=$CONNECTION_ID&giftId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "giftId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-gift?${params}`, {
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
| `giftId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "amount": 1,
        "contact": {
          "id": 1
        },
        "created_at": "string",
        "id": 1,
        "name": "Ava Chen",
        "object": "string",
        "recipient": {
          "name": "Ava Chen"
        },
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.amount` | number |  |
| `data.contact.id` | number |  |
| `data.created_at` | string |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.object` | string |  |
| `data.recipient.name` | string |  |
| `data.updated_at` | string |  |

## Native endpoint

Through the native Monica CRM API, this operation is `GET /gifts/:giftId` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gift.md) for the provider-specific parameters and requirements.

