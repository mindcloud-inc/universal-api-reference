# CardClan: Get Configuration by Card

Retrieves a CardClan integration configuration for a card.

```
GET https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-configuration-by-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-configuration-by-card?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-configuration-by-card?${params}`, {
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
| `cardId` | string | yes | Card ID used to look up the integration configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Integration configuration for the requested card. |
| `message` | string | Configuration lookup result message. |

## Native endpoint

Through the native CardClan API, this operation is `GET /integration/config/by-card` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-configuration-by-card.md) for the provider-specific parameters and requirements.

