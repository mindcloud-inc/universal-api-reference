# Amazon Seller: Create FBM Listings Inventory Report

Creates an FBM listings inventory report in Amazon Seller.

```
POST https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-fbm-listings-inventory-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-fbm-listings-inventory-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportType": "GET_MERCHANT_LISTINGS_DATA_LITER",
  "marketplaceIds": [
    "ATVPDKIKX0DER"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-fbm-listings-inventory-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportType": "GET_MERCHANT_LISTINGS_DATA_LITER",
    "marketplaceIds": ["ATVPDKIKX0DER"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportType` | list | yes | One of: `GET_MERCHANT_LISTINGS_DATA`, `GET_MERCHANT_LISTINGS_DATA_LITER`. Default: `GET_MERCHANT_LISTINGS_DATA_LITER`. |
| `marketplaceIds` | object<string> | yes | Default: `["ATVPDKIKX0DER"]`. |
| `dataStartTime` | date | no |  |
| `dataEndTime` | date | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportOptions` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Seller API returns.

## Native endpoint

Through the native Amazon Seller API, this operation is `POST reports/2021-06-30/reports` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fbm-listings-inventory-report.md) for the provider-specific parameters and requirements.

