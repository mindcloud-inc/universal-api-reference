# Themeforest: List Purchases

Retrieves Envato purchases for the connected account.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/list-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/list-purchases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/list-purchases?${params}`, {
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
| `filterBy` | string | no | Optional Envato purchase list filter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Purchase result page number. |
| `includeAllItemDetails` | boolean | no | Whether Envato should include all item details for each purchase. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "purchases": [
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
| `purchases` | array<object> | Buyer purchases. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v3/market/buyer/list-purchases` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-purchases.md) for the provider-specific parameters and requirements.

