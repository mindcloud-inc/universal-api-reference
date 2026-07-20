# leadtributor.cloud: Offer Lead On Market

Creates a brokerage to offer a lead on a market in leadtributor.cloud.

```
POST https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/offer-lead-on-market
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/offer-lead-on-market" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "5df6897d-0962-4005-adba-12994a984a76",
  "marketId": "REQUIRED_MARKET_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/offer-lead-on-market', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "5df6897d-0962-4005-adba-12994a984a76",
    "marketId": "REQUIRED_MARKET_ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | ID of the lead to offer on the market. Default: `5df6897d-0962-4005-adba-12994a984a76`. |
| `marketId` | string | yes | ID of the market where the lead should be offered. Default: `REQUIRED_MARKET_ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brokerageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brokerageId` | string | ID of the created brokerage. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `POST /markets/:marketId/brokerages` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/offer-lead-on-market.md) for the provider-specific parameters and requirements.

