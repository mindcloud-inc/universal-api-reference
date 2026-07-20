# Prembly: Get Fraud Report Detail

Retrieves a fraud report from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-fraud-report-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-fraud-report-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-fraud-report-detail?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_involved": 1,
      "bank_account_number": "string",
      "bank_name": "Ava Chen",
      "city": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "date_of_birth": "2026-05-07T12:00:00.000Z",
      "date_of_fraud": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "evidence_files": [
        "string"
      ],
      "first_name": "Ava",
      "fraud_category": "string",
      "fraud_category_display": "string",
      "fraud_type": "string",
      "full_name": "Ava Chen",
      "gender": "string",
      "id": "string",
      "id_number": "string",
      "id_type": "string",
      "is_verified": true,
      "last_name": "Chen",
      "middle_name": "Ava Chen",
      "organisation_name": "Ava Chen",
      "report_id": "string",
      "review_notes": "string",
      "reviewed_at": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "status": "string",
      "status_display": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_involved` | number |  |
| `bank_account_number` | string |  |
| `bank_name` | string |  |
| `city` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `date_of_birth` | date |  |
| `date_of_fraud` | date |  |
| `description` | string |  |
| `evidence_files[]` | string |  |
| `first_name` | string |  |
| `fraud_category` | string |  |
| `fraud_category_display` | string |  |
| `fraud_type` | string |  |
| `full_name` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `id_number` | string |  |
| `id_type` | string |  |
| `is_verified` | boolean |  |
| `last_name` | string |  |
| `middle_name` | string |  |
| `organisation_name` | string |  |
| `report_id` | string |  |
| `review_notes` | string |  |
| `reviewed_at` | date |  |
| `state` | string |  |
| `status` | string |  |
| `status_display` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /api/v1/fraud/reports/:reportId/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fraud-report-detail.md) for the provider-specific parameters and requirements.

