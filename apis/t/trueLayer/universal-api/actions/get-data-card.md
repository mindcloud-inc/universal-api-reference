# TrueLayer: Get Data Card

Retrieves a data card from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-card?connectionId=$CONNECTION_ID&card_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "card_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-card?${params}`, {
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
| `card_id` | string | yes | TrueLayer Data API card ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "card_network": "string",
      "card_type": "string",
      "currency": "string",
      "display_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `card_network` | string |  |
| `card_type` | string |  |
| `currency` | string |  |
| `display_name` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /data/v1/cards/:card_id` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-card.md) for the provider-specific parameters and requirements.

