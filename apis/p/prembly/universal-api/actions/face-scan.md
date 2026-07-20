# Prembly: Face Scan

Creates a face scan in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/face-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/face-scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/face-scan', {
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
      "fraud_bank_match": {
        "is_in_fraud_bank": true,
        "total_reports": 1,
        "verified_fraud": true
      },
      "fraud_detected": true,
      "general_analysis": {
        "data_sources_checked": [
          "string"
        ],
        "identity_confidence": 1,
        "identity_consistency": true,
        "primary_identity": {
          "date_of_birth": "2026-05-07T12:00:00.000Z",
          "full_name": "Ava Chen",
          "gender": "string",
          "id_number": "string",
          "id_type": "string",
          "issue_date": "2026-05-07T12:00:00.000Z",
          "match_confidence": 1,
          "state": "string"
        },
        "recommendations": [
          "string"
        ]
      },
      "image_quality_score": 1,
      "multiple_id_analysis": {
        "analysis_summary": "string",
        "fraud_probability": 1,
        "is_suspicious": true,
        "matched_identities": [
          {
            "date_of_birth": "2026-05-07T12:00:00.000Z",
            "full_name": "Ava Chen",
            "gender": "string",
            "id_number": "string",
            "id_type": "string",
            "issue_date": "2026-05-07T12:00:00.000Z",
            "match_confidence": 1,
            "state": "string"
          }
        ],
        "risk_level": "string",
        "total_matches": 1,
        "unique_id_numbers": 1
      },
      "overall_risk_score": 1,
      "processing_time_ms": 1,
      "recommendations": [
        "string"
      ],
      "risk_level": "string",
      "scan_id": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fraud_bank_match.is_in_fraud_bank` | boolean |  |
| `fraud_bank_match.total_reports` | number |  |
| `fraud_bank_match.verified_fraud` | boolean |  |
| `fraud_detected` | boolean |  |
| `general_analysis.data_sources_checked[]` | string |  |
| `general_analysis.identity_confidence` | number |  |
| `general_analysis.identity_consistency` | boolean |  |
| `general_analysis.primary_identity.date_of_birth` | date |  |
| `general_analysis.primary_identity.full_name` | string |  |
| `general_analysis.primary_identity.gender` | string |  |
| `general_analysis.primary_identity.id_number` | string |  |
| `general_analysis.primary_identity.id_type` | string |  |
| `general_analysis.primary_identity.issue_date` | date |  |
| `general_analysis.primary_identity.match_confidence` | number |  |
| `general_analysis.primary_identity.state` | string |  |
| `general_analysis.recommendations[]` | string |  |
| `image_quality_score` | number |  |
| `multiple_id_analysis.analysis_summary` | string |  |
| `multiple_id_analysis.fraud_probability` | number |  |
| `multiple_id_analysis.is_suspicious` | boolean |  |
| `multiple_id_analysis.matched_identities[].date_of_birth` | date |  |
| `multiple_id_analysis.matched_identities[].full_name` | string |  |
| `multiple_id_analysis.matched_identities[].gender` | string |  |
| `multiple_id_analysis.matched_identities[].id_number` | string |  |
| `multiple_id_analysis.matched_identities[].id_type` | string |  |
| `multiple_id_analysis.matched_identities[].issue_date` | date |  |
| `multiple_id_analysis.matched_identities[].match_confidence` | number |  |
| `multiple_id_analysis.matched_identities[].state` | string |  |
| `multiple_id_analysis.risk_level` | string |  |
| `multiple_id_analysis.total_matches` | number |  |
| `multiple_id_analysis.unique_id_numbers` | number |  |
| `overall_risk_score` | number |  |
| `processing_time_ms` | number |  |
| `recommendations[]` | string |  |
| `risk_level` | string |  |
| `scan_id` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /api/v1/fraud/face-scan/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/face-scan.md) for the provider-specific parameters and requirements.

