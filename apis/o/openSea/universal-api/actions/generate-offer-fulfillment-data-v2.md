# OpenSea: Fulfill Offer

Retrieves offer fulfillment data from OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/generate-offer-fulfillment-data-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/generate-offer-fulfillment-data-v2?connectionId=$CONNECTION_ID&offer=%5Bobject%20Object%5D&fulfiller=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offer": "[object Object]",
  "fulfiller": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/generate-offer-fulfillment-data-v2?${params}`, {
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
| `offer` | object | yes |  |
| `fulfiller` | object | yes |  |
| `consideration` | object | no |  |
| `unitsToFill` | number | no | Optional quantity of units to fulfill; defaults to 1 for offers |
| `includeOptionalCreatorFees` | boolean | no | Whether to include optional creator fees in the fulfillment. If creator fees are already required, this is a no-op. Defaults to false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `POST /api/v2/offers/fulfillment_data` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-offer-fulfillment-data-v2.md) for the provider-specific parameters and requirements.

