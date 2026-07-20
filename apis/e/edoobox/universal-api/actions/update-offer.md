# Edoobox: Update Offer

Updates an existing offer in Edoobox.

```
PUT https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/update-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/update-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offerId": "string",
  "vat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/update-offer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offerId": "string",
    "vat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offerId` | string | yes | edoobox offer ID. |
| `vat` | string | yes | Offer VAT mode to set on the offer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "update": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `update` | boolean |  |

## Native endpoint

Through the native Edoobox API, this operation is `PUT /offer/:offer_id` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-offer.md) for the provider-specific parameters and requirements.

