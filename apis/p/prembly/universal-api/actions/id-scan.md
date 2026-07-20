# Prembly: ID Scan

Creates an ID scan in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/id-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/id-scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/id-scan', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "id_number": "string",
      "id_type": "string",
      "is_in_fraud_bank": true,
      "processing_time_ms": 1,
      "recommendations": [
        "string"
      ],
      "risk_level": "string",
      "risk_score": 1,
      "scan_id": "string",
      "search_mode": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "total_reports": 1,
      "unverified_reports": 1,
      "verified_reports": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `id_number` | string |  |
| `id_type` | string |  |
| `is_in_fraud_bank` | boolean |  |
| `processing_time_ms` | number |  |
| `recommendations[]` | string |  |
| `risk_level` | string |  |
| `risk_score` | number |  |
| `scan_id` | string |  |
| `search_mode` | string |  |
| `timestamp` | date |  |
| `total_reports` | number |  |
| `unverified_reports` | number |  |
| `verified_reports` | number |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /api/v1/fraud/id-scan/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/id-scan.md) for the provider-specific parameters and requirements.

