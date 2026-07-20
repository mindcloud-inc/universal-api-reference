# Escrow.com: Generate Partner Report

Creates a partner report in Escrow.com.

```
POST https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/generate-partner-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/generate-partner-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/generate-partner-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionFilters` | object | no | Transaction filters for generating the partner report. |
| `customerFilters` | object | no | Customer filters for generating the partner report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "dateRequestedUtc": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number | Customer ID that requested the report. |
| `dateRequestedUtc` | date | UTC timestamp when the report was requested. |
| `id` | number | Generated partner report ID. |
| `status` | string | Report generation status. |

## Native endpoint

Through the native Escrow.com API, this operation is `POST /partner/reports` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-partner-report.md) for the provider-specific parameters and requirements.

