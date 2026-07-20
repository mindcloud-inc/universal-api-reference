# PayWhirl: Get Card

Retrieves a card from PayWhirl by ID.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-card?connectionId=$CONNECTION_ID&cardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-card?${params}`, {
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
| `cardId` | number | yes | The PayWhirl card ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": "string",
      "country": "string",
      "createdAt": "string",
      "customerId": 1,
      "expDate": "string",
      "funding": "string",
      "gatewayId": 1,
      "gatewayReference": "string",
      "id": 1,
      "last4": "string",
      "title": "string",
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `customerId` | number |  |
| `expDate` | string |  |
| `funding` | string |  |
| `gatewayId` | number |  |
| `gatewayReference` | string |  |
| `id` | number |  |
| `last4` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /card/{id}` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card.md) for the provider-specific parameters and requirements.

