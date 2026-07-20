# Eventzilla: Prepare Checkout

Retrieves checkout details for an event date from Eventzilla.

```
GET https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/prepare-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/prepare-checkout?connectionId=$CONNECTION_ID&eventId=1&dateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "1",
  "dateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/prepare-checkout?${params}`, {
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
| `eventId` | number | yes |  |
| `dateId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discountEnabled": true,
      "paymentOptions": [
        {}
      ],
      "tax": {},
      "taxEnabled": true,
      "tickettypes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discountEnabled` | boolean |  |
| `paymentOptions` | array<object> |  |
| `tax` | object |  |
| `taxEnabled` | boolean |  |
| `tickettypes` | array<object> |  |

## Native endpoint

Through the native Eventzilla API, this operation is `GET /checkout/prepare/:eventid/:dateid` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/prepare-checkout.md) for the provider-specific parameters and requirements.

