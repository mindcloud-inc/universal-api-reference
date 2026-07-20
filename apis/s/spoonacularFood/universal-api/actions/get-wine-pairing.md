# Spoonacular Food: Get Wine Pairing

Retrieves wine pairings from Spoonacular Food for a dish.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-wine-pairing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-wine-pairing?connectionId=$CONNECTION_ID&food=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "food": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-wine-pairing?${params}`, {
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
| `food` | string | yes | Dish, cuisine, or ingredient to pair with wine. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pairedWines": [
        "string"
      ],
      "pairingText": "string",
      "productMatches": [
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
| `pairedWines` | array<string> |  |
| `pairingText` | string |  |
| `productMatches` | array<object> |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/wine/pairing` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wine-pairing.md) for the provider-specific parameters and requirements.

