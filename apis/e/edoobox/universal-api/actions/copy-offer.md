# Edoobox: Copy Offer

Copies an existing offer in Edoobox, with or without dates.

```
POST https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/copy-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/copy-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offerId": "string",
  "category": "string",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/copy-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offerId": "string",
    "category": "string",
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offerId` | string | yes | Source edoobox offer ID to copy. |
| `category` | string | yes | Target edoobox category ID for the copied offer. |
| `number` | string | yes | Offer number for the copied offer. |
| `copyDates` | boolean | no | Whether to copy the source offer dates. Default: `false`. |
| `dateStart` | string | no | Start datetime for copied dates. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Edoobox API returns.

## Native endpoint

Through the native Edoobox API, this operation is `POST /offer/:offer_id/copy` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-offer.md) for the provider-specific parameters and requirements.

