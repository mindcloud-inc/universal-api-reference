# Shippify: Get Delivery Information

Retrieves delivery details from Shippify by ID or reference.

```
GET https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-delivery-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-delivery-information?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-delivery-information?${params}`, {
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
| `id` | string | yes | Shippify delivery identifier or reference ID to query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_status": "string",
      "company": "string",
      "distance": 1,
      "dropoff": {
        "date": "string"
      },
      "id": "string",
      "items": [
        [
          {}
        ]
      ],
      "pickup": {
        "date": "string"
      },
      "recipient": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "referenceId": "string",
      "status": 1,
      "tags": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_status` | string | Delivery status label. |
| `company` | string | Owning company name. |
| `distance` | number | Delivery distance. |
| `dropoff.date` | string | Dropoff datetime. |
| `id` | string | Delivery identifier. |
| `items[]` | array<object> | Delivery item rows. |
| `pickup.date` | string | Pickup datetime. |
| `recipient.email` | string | Recipient email. |
| `recipient.name` | string | Recipient name. |
| `referenceId` | string | Delivery reference identifier. |
| `status` | number | Delivery status code. |
| `tags[]` | array<object> | Delivery tag rows. |

## Native endpoint

Through the native Shippify API, this operation is `GET /v1/deliveries/:id/complete` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-information.md) for the provider-specific parameters and requirements.

